<script>
  import PageHeader from './PageHeader.svelte'
  export let headerText;
  export let image;
</script>

<header class='strike-header' style="background-image: url({image})">
  <div class='page-header-container'>
    <PageHeader text={headerText} />
  </div>
  <ul class='text'>
    <slot></slot>
  </ul>
</header>

<style>
  .page-header-container {
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
    .page-header-container {
      padding: 450px 100px 0px;
    }

    .text {
      padding: 200px 110px 60px;
    }
  }

  @media (max-width: 1300px) {
    .page-header-container {
      padding: 300px 100px 0px;
    }
  }

  @media (max-width: 900px) {
    .page-header-container {
      padding: 250px 40px 0px;
    }

    .text {
      margin-top: -120px;
      padding: 200px 80px 60px;
    }
  }
  
  @media (max-width: 700px) {
    .page-header-container {
      padding: 250px 20px 0px;
    }

    .text {
      margin-top: -40px;
      padding: 100px 40px 60px;
    }
  }
  
  @media (max-width: 500px) {
    .page-header-container {
      padding: 100px 20px 0px;
    }

    .text {
      padding: 100px 40px 60px;
    }
  }
</style>