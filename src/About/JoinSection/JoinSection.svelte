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
      <h6>We’ve got a wide array of options for everyone to participate in the fight for workers rights, including:</h6>
      <ul>
        <li>Participating in social media campaigns</li>
        <li>Protesting exploitative companies with boycotts</li>
        <li>Making your voice heard to your legislators</li>
        <li>Joining or forming unions at your place of work</li>
        <li>Donating to mutual aid organizations</li>
        <li>Supporting in-personal canvassing and events in your area</li>
      </ul>
      <div class='button-container'>
        <Button text='JOIN THE MOVEMENT' href='/join-the-movement' peach />
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

  h6 {
    color: var(--white);
    margin-top: 20px;
  }
  ul {
    margin-top: 20px;
    /* color: var(--white); */
  }

  li {
    color: var(--white);
    font-size: 20px;
    line-height: 30px;
  }
  
  .button-container {
    align-self: flex-start;
    margin-top: 40px;
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