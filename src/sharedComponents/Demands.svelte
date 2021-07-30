<script>
  // TODO: DELETE IF STILL UNUSED
  export let large = false;

  const demands = [
    'Universal healthcare for all',
    '$20 per hour minimum wage',
    '12 weeks paid parental leave',
    '25% corporate tax rate with no loopholes',
    'Four day work week',
    'Net zero emissions by 2030'
  ]
</script>

<section class='demands' class:large >
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
    height: 220px;
  }

  .demand {
    color: var(--white);
    font-size: 26px;
    font-weight: 400;
    line-height: 32px;
    display: flex;
    flex-direction: row;
    align-items: center;
    margin: 0 40px 40px 0;
  }

  p { 
    color: inherit;    
    margin: 0 0 0 15px;
    font-size: inherit;
    line-height: inherit;
  }

  .large {
    padding: 110px 200px 40px;
    height: 400px;
  }

  .large .demand {
    font-size: 36px;
    line-height: 42px;
    max-width: 390px;
  }

  .iconify {
    flex-shrink: 0;
  }

  @media (max-width: 1100px) {
		.demands {
      flex-wrap: nowrap;
      height: unset;
    }

    .large .demand {
      max-width: unset;
    }
	}

  @media (max-width: 900px) {
    .demands {
      padding: 54px 80px 30px;
    }
  }
  
  @media (max-width: 700px) {
    .demands {
      padding: 54px 40px 30px;
    }
  }
  
  @media (max-width: 500px) {
    .demands {
      padding: 40px 20px 20px;
    }

    .large .demand {
      font-size: 28px;
      line-height: 36px;
    }
  }
</style>