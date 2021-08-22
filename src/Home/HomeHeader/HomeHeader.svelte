<script>
  import Button from '../../sharedComponents/Button.svelte'
</script>

<header>  
  <div class='header-left'>
    <h1>Labor Movement X</h1>
      <h5>
        We are here to spark the flame among the working class and fight for significant changes in the workplace.  
      </h5>
      <Button text='JOIN THE MOVEMENT' href='/join-the-movement' blue />
  </div>
  <div class='background-image'>
  </div>
</header>

<style>
  header {
    display: flex;
    flex-direction: row;
    position: relative;
    background-color: var(--red);
  }

  .header-left {
    position: relative;
    display: flex;
    box-sizing: border-box;
    flex-direction: column;
    padding: 70px 50px 100px 172px;
    flex: 1 1 50%;
  }

  h1 {
    color: var(--white);
  }

  h5 {
    margin-bottom: 50px;
    margin-top: 30px;
  }
  
  .background-image {
    flex: 1 1 50%;
    background-image: url('/assets/images/pexels-rosemary-ketchum-1464224.jpeg');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
  }

  @media (max-width: 1100px) {
		.header-left {
      padding: 50px 40px 80px;
    }
	}

  @media (max-width: 900px) {
    .header-left {
      padding: 56px 80px 60px;
    }

    .background-image {
      display: none;
    }
  }

  @media (max-width: 700px) {
    .header-left {
      padding: 56px 40px 60px;
    }
  }

</style>