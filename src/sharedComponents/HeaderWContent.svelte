<script>
  import PageTitle from './PageTitle.svelte'
  export let headerText;
  export let image;
</script>

<header class='strike-header' style="background-image: url({image})">
  <div class='page-title-container'>
    <PageTitle text={headerText} />
  </div>
  <ul class='text'>
    <slot></slot>
  </ul>
</header>

<style>
  .page-title-container {
    padding: 450px 165px 0px;
  }
  
  .strike-header {
    background-size: cover;
    background-position: center -350px;
    background-repeat: no-repeat;
  }

  .text {
    background-color: var(--red);
    padding: 200px 200px 60px;
    margin-top: -120px;
  }

  @media (max-width: 1300px) {
    .page-title-container {
      padding: 450px 100px 0px;
    }

    .text {
      padding: 200px 110px 60px;
    }
  }

  @media (max-width: 1300px) {
    .page-title-container {
      padding: 300px 100px 0px;
    }
  }

  @media (max-width: 900px) {
    .page-title-container {
      padding: 250px 40px 0px;
    }

    .text {
      margin-top: -120px;
      padding: 200px 80px 60px;
    }
  }
  
  @media (max-width: 700px) {
    .page-title-container {
      padding: 250px 20px 0px;
    }

    .text {
      margin-top: -40px;
      padding: 100px 40px 60px;
    }
  }
  
  @media (max-width: 500px) {
    .page-title-container {
      padding: 100px 20px 0px;
    }

    .text {
      padding: 100px 40px 60px;
    }
  }
</style>