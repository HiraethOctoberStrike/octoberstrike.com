<script>
  const planPoints = [
    'Unionizing & Striking  (peacefully)',
    'Submitting a request to join the Labor Movement X discord',
    'Boycotting big businesses (Amazon, Walmart, Target) and shopping small instead',
    'Becoming a State Coordinator',
    "Writing to your state officials or signing the petition <a href='http://chng.it/kNQvH8GXL5' target='_blank'>here</a>",
    'Donating to Mutual Aid',
    'Sharing your story on social media and more!'
  ]
</script>

<section class='plan-section'>
  <div class='top'>
    <img src='assets/images/skyler-gerald-qADoh-Ag7s0-unsplash.jpeg' />
    <div class='plan-content'>
      <h2>We've got a plan:</h2>
      <p>
        The team at Labor Movement X has done weeks of research about the logistics of a national strike. After numerous discussions and leadership meetings, all committees agreed that this will not be a one-day demonstration. This will be a movement that will strike the match and ignite the spark for change. Many of our demands will take time to enact, and we want to ensure that all of our demands are met. Essential workers and all supporters are encouraged to spread the word about this event like wildfire. Tell your friends, family, coworkers, and share your story on social media. 
      </p>
      <p>
        Enough is enough. The people are demanding change, and we are demanding it right now. Follow Labormovementx on social media for more information about how you can get involved! 
      </p>
    </div>
  </div>

  <h5>Key interactions from participants include:</h5>
  <ul>
    {#each planPoints as point}
    <h6><li>{@html point}</li></h6>
    {/each}
  </ul>
</section>

<style>
  .top {
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    align-items: center;
  }

  img {
    margin-right: 30px;
    display: flex;
    flex: 0 2 40%;
    max-height: 500px;
    width: 100%;
    object-fit: contain;
  }

  .plan-content {
    display: flex;
    flex-direction: column;
    flex: 1 0 60%;
    flex-shrink: 1;
  }
  
  p {
    color: var(--dark-grey);
    margin-top: 30px;
  }

  h5 {
    color: var(--black);
    margin: 60px 0 34px;
  }

  ul {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
  }

  h6 {
    display: flex;
    flex: 1 1 40%;
    margin: 0 50px 20px 0;
  }

  li {
    list-style-type: square;
    font-size: 22px;
  }

  @media (max-width: 1000px) {
    .plan-section {
	  	padding: 60px 40px; 
    }

    img {
      flex: 1 1 30%;
    }

    .plan-content {
      flex: unset;
      flex: 1 1 70%;
    } 
  }

  @media (max-width: 700px) {
    .plan-section {
	  	padding: 60px 20px; 
    }
  }
   
  @media (max-width: 700px) {
    .plan-section {
	  	padding: 60px 40px; 
    }

    img {
      display: none;
    }
  }
</style>