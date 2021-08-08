<script>
  import PageHeader from '../../sharedComponents/PageHeader.svelte'
  import Button from '../../sharedComponents/Button.svelte'
</script>

<header>  
  <div class='header-left'>
    <div class='page-header-container'>
      <PageHeader text='Labor Movement X' />
    </div>
    <div class='header-text'>
      <h5>
        LaborMovementX's mission is to spark the flame among the working class to fight for significant change in the workplace.  
      </h5>
      <p>
        We aim to bring attention to the outdated working conditions that many people are subjected to, as well as highlight how these conditions disproportionately affect many marginalized families. We will do this by providing information and resources related to mutual aid, union organizing, and general information about our core values.
      </p>
      <Button text='STRIKE WITH US' href='/strike-with-us' secondary />
    </div>
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

  .page-header-container {
    width: 200%;
  }

  .header-text {
    margin-top: 50px;
    display: flex;
    flex-direction: column;
  }

  h5 {
    margin-bottom: 24px;
  }

  p {
    color: var(--white);
    font-size: 20px;
    font-weight: 500;
    line-height: 30px;
    margin-bottom: 24px;
  }
  
  .background-image {
    flex: 0 1 50%;
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

    .page-header-container {
      width: 100%;
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