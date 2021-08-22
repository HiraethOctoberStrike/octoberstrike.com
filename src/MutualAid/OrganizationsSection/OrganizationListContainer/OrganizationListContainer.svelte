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
  const defaultSelectionText = 'Filter by State'

  const toggleShowMore = () => {
    showMore = !showMore
    filter()
  }

  const filterByState = () => {
    return mutualAidOrgs.filter( org => org.state == selectedState)
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

  const limitResults = (list) => list.slice(0, 10)

  const filter = () => {
    displayOrgs = mutualAidOrgs

    // if state selected, filter by state
    if (selectedState != defaultSelectionText) {
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
      filter()
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
    <button on:click={toggleShowMore}>
      <p>Show {showMore ? "Less" : "More"}</p>
    </button>
  {/if}
{/if}

<style>
  select {
    background-color: var(--light-blue);
    border: 1px solid var(--black);
    color: var(--black);
    padding: 12px 0 12px 20px;
    margin-bottom: 24px;
    font-size: 18px;
    align-self: flex-start;
  }

  option {
    background-color: var(--light-blue);
    padding: 10px;
  }

  button {
    width: 100%;
    text-align: center;
    border: none;
    background-color: var(--lightest-grey);
    padding: 10px;
    transition: 0.1s ease-in;
  }

  button p {
    color: var(--red);
  }

  button:hover {
    background-color: var(--light-grey);
  }
</style>