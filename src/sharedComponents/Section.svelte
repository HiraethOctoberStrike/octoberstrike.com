<script>
  export let width1 = false
  export let width2 = false
  export let width3 = false
  export let width4 = false
  export let width5 = false
  export let navy = false
  export let red = false
  export let lightBlue = false
</script>

<section
  class:width1
  class:width2
  class:width3
  class:width4
  class:width5
  class:navy
  class:red
  class:light-blue={lightBlue}>
  <slot></slot>
</section>

<style>
  section {
	  padding: 60px 165px;
    display: flex;
    flex-direction: column;
  }

  .width1 {
    padding: 60px 298px;
  }

  .width3 {
    padding: 60px 250px;
  }

  .width4 {
    padding: 60px 350px;
  }

  .width5 {
    padding: 60px 400px;
  }

  .navy {
    background-color: var(--navy);
  }
  
  .red {
    background-color: var(--red);
  }

  .light-blue {
    background-color: var(--light-blue);
  }

  
  @media (max-width: 1300px) {
    .width5 {
      padding: 60px 300px;
    }
  }

  @media (max-width: 1100px) {
  	.width1 {
      padding: 60px 160px;
    }

    .width2 {
      padding: 60px 80px;
    }

    .width3 {
      padding: 60px 100px;
    }

    .width4 {
      padding: 60px 160px;
    }

    .width5 {
      padding: 60px 80px;
    }
  }

  @media (max-width: 900px) {
    section {
      padding: 60px 40px; 
    }

     .width1 {
      padding: 60px 100px;
    }

    .width2 {
      padding: 60px 40px;
    }
  }

  @media (max-width: 700px) {
    section {
      padding: 60px 20px; 
    }

    .width1 {
      padding: 60px 80px;
    }

    .width3 {
      padding: 60px 70px;
    }

    .width4 {
      padding: 60px 80px;
    }
  }

  @media (max-width: 500px) {
    .width3 {
      padding: 60px 40px;
    }

    .width4 {
      padding: 60px 40px 0;
    }
  }

</style>