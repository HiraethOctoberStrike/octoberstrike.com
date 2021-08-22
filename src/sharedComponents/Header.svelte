<script>
  import PageTitle from './PageTitle.svelte';

  export let title;
  export let image;
</script>
  
<header style='background-image: url({image});'>
  <div class='page-title-container'>
    <PageTitle text={title} />
  </div>
</header>

<style>
  header {
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
  }

  .page-title-container {
    padding: 60px 120px 200px;
  }

  @media (max-width: 900px) {
    .page-title-container {
      padding: 40px 40px 100px;
    }
  }

  @media (max-width: 700px) {
    .page-title-container {
      padding: 20px 20px 80px;
    }
  }

</style>