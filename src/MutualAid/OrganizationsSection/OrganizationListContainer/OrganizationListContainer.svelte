<script>
  import { onMount } from 'svelte'
  import { csv } from 'd3-request'

  import OrganizationList from './OrganizationList/OrganizationList.svelte'

  const mutualAidCSVPath = 'assets/mutual-aid.csv'

  let mutualAidOrgs
  let displayOrgs
  let filterOptions
  let selectedState
  let showMore = false
  let displayShowMoreButton = false
  const defaultSelectionText = 'All Organizations'

  const toggleShowMore = () => {
    showMore = !showMore
    filter()
  }

  const filterByState = () => {
    return mutualAidOrgs.filter( org => org.state === selectedState)
  }

  const createFilterOptions = () => {
    const states = mutualAidOrgs.map(org => org.state)
    const uniqueStates = states.filter( (value, index, self) => {
      return self.indexOf(value) === index
    })

    // add default selection
    uniqueStates.unshift(defaultSelectionText)

    return uniqueStates
  }

  const limitResults = (list) => {
    return list.slice(0, 10)
  }

  const filter = (mutualAidOrgs) => {
    displayOrgs = mutualAidOrgs
    
    // if state selected, filter by state
    if (selectedState !== defaultSelectionText) {
      displayOrgs = filterByState(mutualAidOrgs)
    }

    displayShowMoreButton = displayOrgs.length > 10

    // if button not displayed, reset show more value to false
    if (!displayShowMoreButton) { showMore = false }

    // if show more enabled, do not limit results
    if (!showMore) { displayOrgs = limitResults(displayOrgs) }
  }

  onMount( () => {
    csv(mutualAidCSVPath, function(error, data) {
      if (error) throw error

      // remove blank lines
      mutualAidOrgs = data.filter( org => Object.values(org).join('') )

      // set initial filter to default
      selectedState = defaultSelectionText
      
      filterOptions = createFilterOptions()
      filter(mutualAidOrgs)
    })
  })

</script>

{#if mutualAidOrgs}
  <select bind:value={selectedState} on:change={filter}>
    {#each filterOptions as state}
      <option value={state}>
        {state}
      </option>
    {/each}
  </select>
  <OrganizationList aidOrgs={displayOrgs} />

  {#if displayShowMoreButton }
    <button on:click={toggleShowMore}>Show {showMore ? "Less" : "More"}</button>
  {/if}
{/if}
