<script>
  import Button from '../../sharedComponents/Button.svelte';
  import Section from '../../sharedComponents/Section.svelte'
</script>

<Section navy narrow>
  <div class='join-container'>
    <div class='img-container'>
      <img class='half-logo' src='assets/images/LMX_Logo_White_HALF.svg' alt='labor movement x logo' />
      <img class='full-logo' src='assets/images/LMX_Logo_White-8.png' alt='labor movement x logo' />
    </div>
    <div class='content-container'>
      <h2>Join the Movement</h2>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Tincidunt lobortis volutpat, est curabitur vestibulum, nec. Tincidunt metus, dui, lorem sed enim ac, est ut imperdiet. Facilisis hac pulvinar posuere convallis adipiscing sit. Sit sit quam tellus, sapien nullam. In eu nunc, ac purus. Urna nunc enim velit tempor sagittis purus cras egestas dignissim. Quis tempor velit velit, felis commodo. Imperdiet faucibus commodo vitae tellus nascetur tristique odio.
      </p>
      <div class='button-container'>
        <Button text='JOIN THE DISCORD' href='https://discord.gg/87k2EY4aRx' peach external />
      </div>
    </div>
  </div>
</Section>
  
<style>
  .join-container {
    display: flex;
    flex-direction: row;
    align-items: center;
  }

  .img-container {
    flex: 1 1 20%;
  }

  .full-logo {
    display: none;
  }

  .content-container {
    display: flex;
    flex-direction: column;
    margin-left: 30px;
    flex: 4 1 80px;
  }

    h2 {
    color: var(--white);
  }

  p {
    margin-top: 20px;
    color: var(--white);
  }
  
  .button-container {
    align-self: flex-start;
    margin-top: 20px;
  }

  @media (max-width: 700px) {
    .join-container {
      flex-direction: column;
    }
    
    .img-container {
      flex: unset;
      height: 200px;
      align-self: flex-start;
    }
    
    .content-container {
      margin-left: unset;
    }

    .half-logo {
      display: none;
    }

    .full-logo {
      display: unset;
    }

    img {
      height: 100%;
    }

    .join-container {
      flex: unset;
    }
  }
</style>