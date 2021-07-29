<script>
  import Button from '../sharedComponents/Button.svelte'
  import HomeHeader from './HomeHeader/HomeHeader.svelte'
  import TimeForChange from './TimeForChange/TimeForChange.svelte'
  import Intersectionality from './Intersectionality/Intersectionality.svelte'
  import Demands from '../sharedComponents/Demands.svelte'

</script>

<HomeHeader />
<TimeForChange />
<Intersectionality />
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
  .section-4 {
    display: flex;
    flex-direction: column;
    padding: 76px 250px 72px;
  }

  .section-4 h1 {
    max-width: 840px;
  }
  
  .red-highlight {
    color: var(--red);
  }

  @media (max-width: 900px) {
    .section-4 {
      padding: 76px 100px 72px;
    }
  }

  @media (max-width: 700px) {
    .section-4 {
      padding: 76px 70px 72px;
    }
  }
 
  @media (max-width: 500px) {
    .section-4 {
      padding: 76px 40px 72px;
    }
  }

</style>