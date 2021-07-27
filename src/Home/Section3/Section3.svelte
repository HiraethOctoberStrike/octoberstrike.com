<script>
  const demands = [
    {
      title: 'Universal Healthcare',
      snippet: 'Pharmaceutical companies are extorting patients for medications',
    },
    {
      title: 'Paid Parental Leave',
      snippet: 'The United States is the only developed country that requires zero paid time off for maternity leave.',
    },
    {
      title: 'Coporate Accountability in Climate Change',
      snippet: 'Only 100 corporations are responsible for 71% of all global carbon emissions.',
    },
    {
      title: 'Corporate Tax Evasion',
      snippet: 'Amazon paid $0 in taxes in 2017 and 2018.',
    },
    {
      title: 'Overworking & Burnout',
      snippet: '78% of employees with 5 day weeks are less happy and more stressed than those with 4 day weeks.',
    },
    {
      title: 'Minimum Wage & Income Inequality',
      snippet: '40 million Americans live at\, or below the national poverty line. Current minimum wages are poverty wages.',
    }
  ]

  const intersectionality = []
</script>

<section>
  <h1>
    The U.S. government is not serving its people. Now is the time for change.
  </h1>
  <div class='demands'>
    {#each demands as { title, snippet }, i }
      <div class='demand' class:darken={[1, 2, 5].includes(i)}>
        <h3>{title}</h3>
        <h5>{snippet}</h5>
      </div>
    {/each}
  </div>
</section>

<style>
  section {
    padding: 71px 165px 105px;
  }

  .demands {
    display: flex;
    display: row;
    flex-wrap: wrap;
    width: 100%;
  }

  .demand {
    padding: 35px 57px 26px 44px;
    box-sizing: border-box;
    width: 50%;
    background-color: var(--light-grey);
    margin-bottom: 46px;
  }

  .darken {
    background-color: var(--medium-grey1);
  }

  h3 {
    max-width: 450px;
  }

  h5 {
    max-width: 450px;
  }
</style>