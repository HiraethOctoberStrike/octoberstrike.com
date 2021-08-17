<script>
  import Button from '../../sharedComponents/Button.svelte'
  import Section from '../../sharedComponents/Section.svelte'
</script>

<Section>
  <div class='mutual-aid-container'>
    <div class='img-container'>
      <img src='assets/images/toa-heftiba-6bKpHAun4d8-unsplash.jpeg' />
    </div>
    <div class='plan-content'>
      <h2>Mutual Aid</h2>
      <p>
        Labor Movement X is in the process of building and establishing stronger relationships with not just unions, but the entire community. Ensuring that essential workers have a safety net for the potential ramifications of striking is our top priority, and we are working night and day to make that happen. We plan to collaborate with nonprofit groups, mutual aid organizations, farmers, and any other individual willing to volunteer! There are several committees working behind the scenes to make this event possible, but our mutual aid committee is by far the most important. During this time, we hope that every family will feel safe and supported within their community.  
      </p>
      <p>
        If you have questions about Labor Movement X’s effort in financially supporting communities across the nation, email <a href='mailto: labormovementXMA@gmail.com'>labormovementXMA@gmail.com</a>. A member of the committee can assist you with finding resources in your area, or help you get involved!
      </p>
      <Button text='LEARN MORE' href='/mutual-aid' red />
    </div>
  </div>
</Section>

<style>
  .mutual-aid-container {
    display: flex;
    flex-direction: row;
    align-items: center;
    width: 100%;
  }

  .img-container {
    flex: 0 1 50%;
    margin-right: 50px;
  }
  img {
    width: 100%;
  }

  .plan-content {
    display: flex;
    flex-direction: column;
    flex: 1 0 50%;
    flex-shrink: 1;
  }

  h2 {
    margin-bottom: 20px;
  }
  
  p {
    color: var(--dark-grey);
    margin-bottom: 30px;
  }

  @media (max-width: 1100px) {
    .mutual-aid-container {
      flex-direction: column;
    }

    img {
      margin: 0 0 50px;
      flex: unset;
    }

    .plan-content {
      flex: unset;
    } 
  }
</style>