<script>
  import { demands } from '../../copy.js'
  import Card from '../../sharedComponents/Card.svelte'
</script>

<section class='time-for-change'>
  <h2>
    The U.S. government is not serving its people. Now is the time for change.
  </h2>
  <div class='demands'>
    {#each demands as { title, snippet }, i }
      <Card {title} {snippet} 
        red={[0, 4].includes(i)}
        navy={[3, 7].includes(i)} />
    {/each}
  </div>
</section>

<style>
  .time-for-change {
    background-color: var(--white);
  }

  .demands {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    box-sizing: border-box;
    margin: -16px;
  }

  h2 {
  	margin-bottom: 50px;
  }

  p {
    color: var(--black);
  }
</style>