<script>
  import { timeForChange } from '../../copy.js'
  import Card from '../../sharedComponents/Card.svelte'
</script>

<section class='time-for-change'>
  <h2>
    The U.S. Government is not serving its people. Now is the time for change.
  </h2>
  <div class='demands'>
    {#each timeForChange as { title, subtitle, snippet }, i }
      <Card {title} red={[0, 4].includes(i)} navy={[3, 7].includes(i)}>
        <div>
          <h6>{subtitle}</h6>
          <p>{@html snippet}</p>
        </div>
      </Card>
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

  h6 {
    margin-bottom: 18px;
  }
</style>