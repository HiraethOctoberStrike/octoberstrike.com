<script>
  import { demands } from '../../copy.js'
  import Button from '../../sharedComponents/Button.svelte'
</script>

<header>
  <div class='header-container'>
    <h1>Labor Movement X</h1>
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
  <div class='background-image'>
  </div>
</header>

<style>
  header {
    position: relative;
    background-color: var(--red);
    overflow: auto;
  }

  .header-container {
    position: relative;
    z-index: 1;
    margin: 48px 128px 0px;
    background-color: var(--white);
    padding: 30px;
    box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.25);
    display: inline-block;
  }

  .header-text {
    position: relative;
    display: flex;
    flex-direction: column;
    padding: 70px 50px 100px 172px;
    z-index: 1;
    width: 50%;
    box-sizing: border-box;
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
    width: 50%;
    height: 100%;
    position: absolute;
    right: 0;
    top: 0;

    background-image: url('/assets/images/pexels-rosemary-ketchum-1464224.jpeg');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
  }

  @media (max-width: 1100px) {
		.header-text {
      width: 100%;
    }

    .background-image {
      display: none;
    }
	}

  @media (max-width: 900px) {
    .header-container {
      margin: 48px 40px 0px;
    }

    .header-text {
      padding: 56px 80px 60px;
    }
  }

  @media (max-width: 700px) {
    .header-container {
      margin: 48px 20px 0px;
    }

    .header-text {
      padding: 56px 40px 60px;
    }
  }

</style>