<script>
  const demands = [
    {
      title: 'Universal Healthcare',
      subheader: 'Pharmaceutical companies are extorting patients for medications',
      snippet: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Volutpat risus, nibh id egestas. Iaculis ultrices magna ac sed scelerisque blandit in ridiculus accumsan. Ac cursus diam posuere lectus.'
    },
    {
      title: 'Paid Parental Leave',
      subheader: 'The United States is the only developed country that requires zero paid time off for maternity leave.',
      snippet: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Volutpat risus, nibh id egestas. Iaculis ultrices magna ac sed scelerisque blandit in ridiculus accumsan. Ac cursus diam posuere lectus.'
    },
    {
      title: 'Coporate Accountability in Climate Change',
      subheader: 'Only 100 corporations are responsible for 71% of all global carbon emissions.',
      snippet: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Volutpat risus, nibh id egestas. Iaculis ultrices magna ac sed scelerisque blandit in ridiculus accumsan. Ac cursus diam posuere lectus.'
    },
    {
      title: 'Corporate Tax Evasion',
      subheader: 'Amazon paid $0 in taxes in 2017 and 2018.',
      snippet: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Volutpat risus, nibh id egestas. Iaculis ultrices magna ac sed scelerisque blandit in ridiculus accumsan. Ac cursus diam posuere lectus.'
    },
    {
      title: 'Overworking & Burnout',
      subheader: '78% of employees with 5 day weeks are less happy and more stressed than those with 4 day weeks.',
      snippet: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Volutpat risus, nibh id egestas. Iaculis ultrices magna ac sed scelerisque blandit in ridiculus accumsan. Ac cursus diam posuere lectus.'
    },
    {
      title: 'Minimum Wage & Income Inequality',
      subheader: '40 million Americans live at\, or below the national poverty line. Current minimum wages are poverty wages.',
      snippet: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Volutpat risus, nibh id egestas. Iaculis ultrices magna ac sed scelerisque blandit in ridiculus accumsan. Ac cursus diam posuere lectus.'
    }
  ]

  const intersectionality = [
    {
      title: "Race in the Working Class",
      snippet: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Volutpat risus, nibh id egestas. Iaculis ultrices magna ac sed scelerisque blandit in ridiculus accumsan. Ac cursus diam posuere lectus.'
    },
    {
      title: "Disability in the Working Class",
      snippet: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Volutpat risus, nibh id egestas. Iaculis ultrices magna ac sed scelerisque blandit in ridiculus accumsan. Ac cursus diam posuere lectus.'
    },
    {
      title: "Gender in the Working Class",
      snippet: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Volutpat risus, nibh id egestas. Iaculis ultrices magna ac sed scelerisque blandit in ridiculus accumsan. Ac cursus diam posuere lectus.'
    }
  ]
</script>

<section class='time-for-change'>
  <h1>
    The U.S. government is not serving its people. Now is the time for change.
  </h1>
  <div class='demands'>
    {#each demands as { title, subheader, snippet }, i }
      <div class='demand' class:darken={[1, 2, 5].includes(i)}>
        <h3>{title}</h3>
        <h5>{subheader}</h5>
        <h6>{snippet}</h6>
      </div>
    {/each}
  </div>

  <h2>
    The fight for the rights of the working class is an intersectional issue.
  </h2>
  <div class='intersectionalities'>
    {#each intersectionality as { title, snippet }, i }
      <div class='intersectionality' class:darken={i ==1}>
        <h3>{title}</h3>
        <h6>{snippet}</h6>
      </div>
    {/each}
  </div>
</section>

<style>
  .time-for-change {
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
    padding: 54px 57px 70px;
    box-sizing: border-box;
    width: 50%;
    background-color: var(--light-grey);
    margin-bottom: 46px;
  }

  .intersectionalities {
    display: flex;
    flex-direction: row;
    margin: -16px;
  }

  .intersectionality {
    padding: 29px;
    background-color: var(--light-grey);
    flex: 1 1;
    margin: 16px;
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

  @media (max-width: 1100px) {
    .demands {
      flex-direction: column;
      flex-wrap: nowrap;
	  }
    
    .demand {
      width: 100%;
      margin-bottom: 0;
    }
    
    .demand:nth-child(odd) {
      background-color: var(--light-grey);
    }
    
    .demand:nth-child(even) {
      background-color: var(--medium-grey1);
      margin-bottom: 24px;
    }
    
    .intersectionalities {
      flex-wrap: wrap;
      margin: -12px;
    }
    
    .intersectionality {
      flex: 1 0 30%;
      margin: 12px;
    }
    
    @media (max-width: 900px) {
      .time-for-change {
        padding: 71px 40px 105px; 
      }
    }
    
    @media (max-width: 700px) {
      .time-for-change {
        padding: 71px 20px 105px; 
      }

      .demand {
        padding: 40px;
      }

      .demand:nth-child(even) {
        margin-bottom: 12px;
      }

      .intersectionalities {
        margin: -6px;
      }

      .intersectionality {
        padding: 40px;
        margin: 6px;
      }
    }

    @media (max-width: 500px) {
      .demand {
        padding: 30px 20px;
      }

      .intersectionality {
        padding: 20px;
        margin: 6px;
      }
    }
  }
  </style>