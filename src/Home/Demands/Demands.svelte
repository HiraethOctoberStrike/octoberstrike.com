<script>

  const demands = [
    'Universal healthcare for all',
    '$20 per hour minimum wage',
    '12 weeks paid parental leave',
    '25% corporate tax rate with no loopholes',
    'Four day work week',
    'Net zero emissions by 2030'
  ]
</script>

<section class='demands'>
  {#each demands as demand }
    <div class='demand'>
      <span class="iconify" data-icon="mdi-check-circle"></span>
      <p>{demand}</p>
    </div>
  {/each}
</section>

<style>
  .demands {
    padding: 54px 165px 5px;
    background-color: var(--red);
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    justify-content: flex-start;
    align-items: flex-start;
    height: 200px;
  }

  .demand {
    color: var(--white);
    font-size: 26px;
    font-weight: 400;
    line-height: 32px;
    flex-grow: 0;
    display: flex;
    flex-direction: row;
  }

  p { 
    color: inherit;    
    margin: 0 15px 40px;
  }
</style>