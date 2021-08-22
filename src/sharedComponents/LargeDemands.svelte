<script>
  import { demands } from '../copy.js'
</script>

<div class='demands'>
  <div class='column'>
    {#each demands[0] as { numeral, title } }
      <div class='demand'>
        <h2>{numeral}</h2>
        <h5>{title}</h5>
      </div>
    {/each}
  </div>
  <div class='column'>
    {#each demands[1] as { numeral, title } }
      <div class='demand'>
        <h2>{numeral}</h2>
        <h5>{title}</h5>
      </div>
    {/each}
  </div>
</div>

<style>
  .demands {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
  }

  .demand {
    display: flex;
    flex-direction: row;
    align-items: center;
    margin-bottom: 50px ;
  }

  .column {
    flex: 1 1 50%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }

  h2 {
    font-family: 'Brix-Slab', serif;
    font-weight: 900;
    font-size: 72px;
    color: var(--peach);
    width: 114px;
    opacity: 0.6;
    text-align: center;
    position: relative;
    right: -40px;
    margin-left: -40px;
  }

  h5 {
    color: var(--white);
    z-index: 1;
    flex: 1 0;
  }

  @media (max-width: 800px) {
    .column {
      flex: 1 1 100%;
    }
    
    .demand {
      margin-bottom: 30px
    }
  }
</style>