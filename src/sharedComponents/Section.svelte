<script>
  export let narrower = false
  export let demands = false
  export let narrow = false
  export let narrowest = false
  export let navy = false
  export let red = false
  export let lightBlue = false
</script>

<section
  class:narrower
  class:demands
  class:narrow
  class:narrowest
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

  .narrowest {
    padding: 60px 400px;
  }

  .narrower {
    padding: 60px 300px;
  }

  .narrow {
    padding: 60px 250px;
  }

  .demands {
    padding: 60px 200px;
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
    .narrowest {
      padding: 60px 300px;
    }
  }

  @media (max-width: 1100px) {
    .narrowest {
      padding: 60px 200px;
    }

  	.narrower {
      padding: 60px 160px;
    }

    .narrow {
      padding: 60px 100px;
    }

    .demands {
      padding: 60px 80px;
    }
  }

  @media (max-width: 900px) {
    .narrowest {
      padding: 60px 160px;
    }

    .narrower {
      padding: 60px 100px;
    }

    section, .demands {
      padding: 60px 40px; 
    }
  }

  @media (max-width: 700px) {
    .narrowest {
      padding: 60px 100px;
    }

    .narrower {
      padding: 60px 80px;
    }
    
    .narrow {
      padding: 60px 70px;
    }
    
    section {
      padding: 60px 20px; 
    }
  }

  @media (max-width: 500px) {
    .narrowest {
      padding: 60px 80px;
    }

    .narrow {
      padding: 60px 40px;
    }
  }

</style>