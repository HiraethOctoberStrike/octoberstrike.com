<script>
  import { transparencyDemands } from '../../copy.js'
</script>
  
<section class='transparency-section'>
  <div class='column'>
    {#each transparencyDemands[0] as { numeral, demand } }
      <div class='demand'>
        <h4>{numeral}</h4>
        <h5 class='demand-text'>{demand}</h5>
      </div>
    {/each}
  </div>
  <div class='column'>
    {#each transparencyDemands[1] as { numeral, demand } }
      <div class='demand'>
        <h4>{numeral}</h4>
        <h5 class='demand-text'>{demand}</h5>
      </div>
    {/each}
  </div>
</section>

<style>
  .transparency-section {
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
    font-size: 32px;
    width: 50px;
    opacity: 0.6;
    text-align: center;
  }

  h5 {
    flex: 1 0;
  }


  @media (max-width: 1100px) {
    .transparency-section {
      padding: 60px 80px;
    }
  }

  @media (max-width: 900px) {
    .transparency-section {
      padding: 60px 40px;
    }
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

  @media (max-width: 550px) {
    .transparency-section {
      height: unset;
      padding: 60px 80px;
    }
  }
  
  @media (max-width: 400px) {
    .transparency-section {
      height: unset;
      padding: 60px 40px;
    }
  }
</style>