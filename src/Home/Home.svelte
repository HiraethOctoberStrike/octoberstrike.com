<script>
  import Button from '../sharedComponents/Button.svelte'
  import TimeForChange from './TimeForChange/TimeForChange.svelte'
  import Demands from './Demands/Demands.svelte'

</script>

<section class='section-1'>
  <h4>October 15 2021</h4>
  <h1>National General Strike</h1>
  <p>
    Lorem ipsume dolor sit amet, consectetur adipiscing elit. Ornare duis lacus neque adipiscing aliquam molestie fermentum. Eget commodo quisque non, porta. In congue sociis donec vel laoreet in pharetra. Vitae habitant et.
  </p>
  <Button text='STRIKE WITH US' href='/strike-with-us' />
</section>
<Demands />
<TimeForChange />
<section class='section-4'>
  <h1>
    We’ve voted and argued, but now it’s time to <span class='red-highlight'>strike</span>.
  </h1>
  <p>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Volutpat risus, nibh id egestas. Iaculis ultrices magna ac sed scelerisque blandit in ridiculus accumsan. Ac cursus diam posuere lectus. Pretium, quisque leo risus sed. Auctor penatibus non laoreet habitant sem cras faucibus commodo sit. Scelerisque enim, non sit morbi id. Tincidunt eget leo risus posuere et volutpat pharetra odio. 
  </p>
  <Button text='STRIKE WITH US' href='/strike-with-us' secondary={true} />
</section>

<style>

  section {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
  }

  .section-1 {
    padding: 134px 165px 104px;
    background-color: var(--light-grey);
  }

  .section-1 p {
    max-width: 550px;
  }
  
  .section-4 {
    padding: 76px 250px 72px;
  }

  .section-4 h1 {
    max-width: 840px;
  }
  
  .red-highlight {
    color: var(--red);
  }

  @media (max-width: 900px) {
    .section-1 {
      padding: 134px 80px 104px;
    }

    .section-4 {
      padding: 76px 100px 72px;
    }
  }

  @media (max-width: 700px) {
    .section-1 {
      padding: 134px 40px 104px;
    }

    .section-4 {
      padding: 76px 70px 72px;
    }
  }

</style>