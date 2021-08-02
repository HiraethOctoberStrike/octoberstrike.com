<script>
  import Button from '../../sharedComponents/Button.svelte'
</script>

<section class='mutual-aid-section'>
    <img src='assets/images/toa-heftiba-6bKpHAun4d8-unsplash.jpeg' />
  <div class='plan-content'>
    <h2>Mutual Aid</h2>
    <p>
      Labor Movement X is in the process of establishing and building stronger relationships with not only unions, but also the community. Mutual Aid and ensuring that essential workers who would like to strike are able to do so without stressing over their bills, is a priority of Labor Movement X. There are several committees behind the scenes to make this event possible, but our Mutual Aid committee is by far the most important. 
    </p>
    <p>
      If you have questions about Labor Movement X’s effort in financially supporting communities across the nation, email <a href='mailto: labormovementXMA@gmail.com'>labormovementXMA@gmail.com</a>. A member of the committee can assist you with finding resources in your area, or help you get involved!
      
    </p>
    <Button text='LEARN MORE' href='/mutual-aid' tertiary />
  </div>
</section>

<style>

  .mutual-aid-section {
    position: relative;
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    align-items: center;
  }

  img {
    margin-right: 50px;
    display: flex;
    flex: 0 2 50%;
    max-height: 500px;
    width: 100%;
    object-fit: contain;
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

  @media (max-width: 1000px) {
    .mutual-aid-section {
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