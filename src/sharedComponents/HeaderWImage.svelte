<script>
  export let headerText;
  export let image;
</script>

<header class='strike-header' style="background-image: url({image})">
  <div class='h1-container'>
    <h1>{headerText}</h1>
  </div>
  <ul class='text'>
    <slot></slot>
  </ul>
</header>

<style>
  .h1-container {
    display: inline-block;
    padding: 30px;
    background-color: var(--white);
    margin: 450px 165px -50px;
    box-sizing: border-box;
  }
  
  .strike-header {
    background-size: cover;
    background-position: center -350px;
    background-repeat: no-repeat;
  }

  .text {
    background-color: var(--red);
    padding: 200px 200px 60px;
    margin-top: -20px;
  }

  @media (max-width: 1635px) {
    .text {
      margin-top: -80px;
    }
  }

  @media (max-width: 1300px) {
    .h1-container {
      margin: 450px 100px -50px;
    }

    .text {
      padding: 200px 120px 60px;
      margin-top: -70px;
    }
  }

  @media (max-width: 1100px) {
    .text {
      margin-top: -70px;
    }
  }
  
  @media (max-width: 900px) {

    .h1-container {
      margin: 150px 40px -50px;
    }

    .text {
      margin-top: -120px;
      padding: 220px 80px 60px;
    }
  }
  
  @media (max-width: 700px) {

    .h1-container {
      margin: 150px 20px -50px;
    }

    .text {
      margin-top: -10px;
      padding: 100px 40px 60px;
    }
  }
  
  @media (max-width: 500px) {

    .h1-container {
      margin: 100px 20px -50px;
      padding: 16px 16px 12px;
    }

    .text {
      margin-top: -40px;
      padding: 100px 60px 60px;
    }
  }

</style>