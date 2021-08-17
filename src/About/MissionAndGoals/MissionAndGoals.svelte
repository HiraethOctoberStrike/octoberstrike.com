<script>
  import Button from '../../sharedComponents/Button.svelte';
  import Section from '../../sharedComponents/Section.svelte'

</script>

<Section demandsPadding>
  <div class='mission-and-goals-section'>
    <div class='mission'>
      <h4>Our Mission</h4>
      <p>
        We aim to organize our collective power - our voices, our labor, our dollars - to take concrete, sweeping action needed to save this country from continued collapse. After a year and a half of a pandemic and on the brink of environmental devastation we can no longer afford to be patient. To ask for change and wait for those with power and influence to save us all. We’re coming together to demand progress now.
      </p>
    </div>
      
    <div class='goals'>
      <h4>Our Goals</h4>
      <p>
        Passage of legislation surrounding our <a href='/home'>X demands</a> by October 14th, to be enacted January 1st, 2022. 
      </p>
      <div class='button-container'>
        <Button text='OUR DEMANDS' href='/home' white smallText />
      </div>
      <p>
        Raising $20 billion for mutual aid funds by October 14th, from the wealthiest Americans who have long benefited off of our labor.
      </p>
      <div class='button-container'>
        <Button text='MUTUAL AID' href='/mutual-aid' white smallText />
      </div>
    </div>
  </div>
</Section>

  <style>
    .mission-and-goals-section {
      display: flex;
      flex-direction: row;
      margin: -60px -20px 0px;
    }

    .mission, .goals {
      display: flex;
      flex-direction: column;
      flex: 1 1 50%;
      border: 1px solid var(--navy);
      padding: 40px;
      margin: 20px;
      border-radius: 12px;
    }

    h4 {
      margin-bottom: 36px;
    }

    .goals p {
      margin-bottom: 10px;
    }

    .button-container {
      align-self: flex-start;
      margin: 0 0 30px -30px;
    }

    .button-container:last-child {
      margin-bottom: 0;
    }

    @media (max-width: 900px) {
      .mission, .goals {
        padding: 20px;
      }
      .button-container {
        margin: 0 0 14px -14px;
      }
    }

    @media (max-width: 700px) {
      .mission-and-goals-section {
        flex-direction: column;
      }
    }
  </style>