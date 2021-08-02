<script>
  import Button from '../../sharedComponents/Button.svelte'
</script>

<section class='weve-voted-section'>
  <h1>
    We’ve waited, we’ve asked, but now it’s time to <span class='emphasize'>demand</span>.
  </h1>
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