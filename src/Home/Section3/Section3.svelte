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

  const intersectionality = [
    {
      title: "Race in the Working Class"
    },
    {
      title: "Disability in the Working Class"
    },
    {
      title: "Gender in the Working Class"
    }
  ]
</script>

<section class='section-3'>
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

  <h2>
    The fight for the rights of the working class is an intersectional issue.
  </h2>
  <div class='intersectionalities'>
    {#each intersectionality as { title }, i }
      <div class='intersectionality' class:darken={i ==1}>
        <h3>{title}</h3>
      </div>
    {/each}
  </div>
</section>

<style>
  .section-3 {
    padding: 71px 165px 105px;
    background-color: var(--lightest-grey);
  }

  .demands {
    display: flex;
    flex-direction: row;
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

  .intersectionalities {
    display: flex;
    flex-direction: row;
    width: 100%;
  }

  .intersectionality {
    padding: 29px 29px 44px;
    background-color: var(--light-grey);
  }

  .intersectionality:nth-child(2) {
    margin: 0 32px;
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