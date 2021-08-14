<script>
  import PageTitle from './PageTitle.svelte';

  export let title
</script>
  
<header>
  <div class='page-title-container'>
    <PageTitle text={title} />
  </div>
</header>

<style>
  header {
    background-image: url('/assets/images/pexels-rosemary-ketchum-1464224.jpeg');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
  }

  .page-title-container {
    padding: 60px 120px 200px;
  }

  @media (max-width: 900px) {
    .page-title-container {
      padding: 40px 80px 100px 40px;
    }
  }

  @media (max-width: 700px) {
    .page-title-container {
      padding: 20px 80px 80px 20px;
    }
  }

</style>