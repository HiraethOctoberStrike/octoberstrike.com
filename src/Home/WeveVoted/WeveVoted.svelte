<script>
  import Button from '../../sharedComponents/Button.svelte'
</script>

<section class='weve-voted-section'>
  <h1>
    We’ve voted and argued, but now it’s time to <span class='red-highlight'>strike</span>.
  </h1>
  <p>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Volutpat risus, nibh id egestas. Iaculis ultrices magna ac sed scelerisque blandit in ridiculus accumsan. Ac cursus diam posuere lectus. Pretium, quisque leo risus sed. Auctor penatibus non laoreet habitant sem cras faucibus commodo sit. Scelerisque enim, non sit morbi id. Tincidunt eget leo risus posuere et volutpat pharetra odio. 
  </p>
</section>

<style>
  .weve-voted-section {
    display: flex;
    flex-direction: column;
    padding: 60px 250px;
  }

  h1 {
    max-width: 840px;
    margin-bottom: 40px;
  }

  .red-highlight {
    color: var(--red);
  }

  @media (max-width: 1100px) {
    .weve-voted-section {
      padding: 60px 100px;
    }
  }

  @media (max-width: 700px) {
    .weve-voted-section {
      padding: 60px 70px;
    }
  }
 
  @media (max-width: 500px) {
    .weve-voted-section {
      padding: 60px 40px;
    }
  }
</style>