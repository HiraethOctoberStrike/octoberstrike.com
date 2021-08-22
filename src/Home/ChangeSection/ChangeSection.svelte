<script>
  import { demands } from '../../copy.js'
  import DemandCard from './DemandCard/DemandCard.svelte'
  import Section from '../../sharedComponents/Section.svelte'
</script>

<Section>
  <h2>
    The U.S. Government is not serving its people. Now is the time for change.
  </h2>
  <div class='demands'>
    {#each demands.flat() as demand }
      <DemandCard {demand} />
    {/each}
  </div>
</Section>

<style>
  .demands {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    box-sizing: border-box;
    margin: -25px;
  }

  h2 {
  	margin-bottom: 50px;
  }
</style>