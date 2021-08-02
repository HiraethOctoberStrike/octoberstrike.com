<script>
  const planPoints = [
    'Unionizing & Striking  (peacefully)',
    'Submitting a request to join the Labor Movement X discord',
    'Boycotting big businesses (Amazon, Walmart, Target) and shopping small instead',
    'Becoming a State Coordinator',
    'Writing to your state officials or signing the petition here',
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
        The team at Labor Movement X thought long and hard about the logistics’ of what would happen on October 15.  After numerous leaderships meetings, all committees came to the same agreement—this is not a one-day demonstration, but a movement that will strike the match and ignite the spark for change. This is because many of Labor Movement X’s demands take time. Essential workers are encouraged to spread the word about this event like wild fire. Tell friends, family, coworkers, and share your “X” on social media. 
      </p>
      <p>
        After all, enough is enough. We the people are demanding change. Not change in 10 years, but right now. Follow #themovement on social media for more information about how you can get involved and carry the torch in your area!
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