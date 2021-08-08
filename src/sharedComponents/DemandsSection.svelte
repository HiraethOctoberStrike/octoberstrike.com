<script>
  import Section from './Section.svelte'

  export let demands
</script>

<Section navy wide>
  <div class='demands'>
    <div class='column'>
      {#each demands[0] as { numeral, demand } }
        <div class='demand'>
          <h4>{numeral}</h4>
          <h5 class='demand-text'>{demand}</h5>
        </div>
      {/each}
    </div>
    <div class='column'>
      {#each demands[1] as { numeral, demand } }
        <div class='demand'>
          <h4>{numeral}</h4>
          <h5 class='demand-text'>{demand}</h5>
        </div>
      {/each}
    </div>
  </div>
</Section>

<style>
  .demands {
    background-color: var(--navy);
    box-sizing: border-box;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
  }
  
  .column {
    flex: 1 1 50%;
  }

  .demand {
    display: flex;
    flex-direction: row;
    align-items: center;
    font-size: 28px;
    margin: 0 32px 32px 0;
    color: var(--white);
    flex-shrink: 1;
  }

  h4 {
    font-family: 'Brix-Slab', serif;
    font-weight: 900;
    color: var(--peach);
    margin-right: 18px;
    width: 50px;
    opacity: 0.6;
    text-align: center;
  }

  h5 {
    flex: 1 0;
  }

  @media (max-width: 800px) {
    .demand {
      font-size: 18px;
      margin-bottom: 16px;
    }

    h5 {
      font-size: 18px;
    }
    
    .column {
      flex: 1 1 100%;
    }
  }
</style>