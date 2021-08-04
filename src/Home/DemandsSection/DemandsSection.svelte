<script>
  import { demands } from '../../copy.js'
</script>

<section class='demands-section'>
  <div class='column'>
    {#each demands[0] as demand }
      <div class='demand'>
        <span class="iconify" data-icon="mdi-check-circle"></span>
        <h5 class='demand-text'>{demand}</h5>
      </div>
    {/each}
  </div>
  <div class='column'>
    {#each demands[1] as demand }
      <div class='demand'>
        <span class="iconify" data-icon="mdi-check-circle"></span>
        <h5 class='demand-text'>{demand}</h5>
      </div>
    {/each}
  </div>
</section>

<style>
  .demands-section {
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

  .iconify {
    flex-shrink: 0;
    margin-right: 8px;
  }

  h5 {
    margin: 0 0 0 15px;
  }


  @media (max-width: 1100px) {
    .demands-section {
      padding: 60px 80px;
    }
  }

  @media (max-width: 900px) {
    .demands-section {
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
    .demands-section {
      height: unset;
      padding: 60px 80px;
    }
  }
  
  @media (max-width: 400px) {
    .demands-section {
      height: unset;
      padding: 60px 40px;
    }
  }
</style>