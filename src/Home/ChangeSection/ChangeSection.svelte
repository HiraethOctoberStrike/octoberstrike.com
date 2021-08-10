<script>
  import { timeForChange } from '../../copy.js'
  import Card from '../../sharedComponents/Card.svelte'
  import Section from '../../sharedComponents/Section.svelte'
</script>

<Section>
  <h2>
    The U.S. Government is not serving its people. Now is the time for change.
  </h2>
  <div class='demands'>
    <div class='column'>
      {#each timeForChange[0] as { title, subtitles, snippet }, i }
        <Card {title} red={i % 2 === 0}>
          <div>
            {#each subtitles as subtitle}
              <h6>{@html subtitle}</h6>
            {/each}
            <p>{@html snippet}</p>
          </div>
        </Card>
      {/each}
    </div>
    <div class='column'>
      {#each timeForChange[1] as { title, subtitles, snippet }, i }
        <Card {title} navy={i % 2 !== 0}>
          <div>
            {#each subtitles as subtitle}
              <h6>{@html subtitle}</h6>
            {/each}
            <p>{@html snippet}</p>
          </div>
        </Card>
      {/each}
    </div>
  </div>
</Section>

<style>
  .demands {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    box-sizing: border-box;
    margin: -16px;
  }

  .column {
    display: flex;
    flex-direction: column;
    flex: 1 1 50%;
    align-self: flex-start;
  }

  h2 {
  	margin-bottom: 50px;
  }

  h6 {
    margin-bottom: 18px;
  }

  @media (max-width: 1100px) {
    .column {
      flex: 1 1 100%;
    }
  }
</style>