<section class='plan-section'>
  <img src='assets/images/skyler-gerald-qADoh-Ag7s0-unsplash.jpeg' />
  <div class='plan-content'>
    <h2>We've got a plan:</h2>
    <p>
      October Labor Movement is run by passionate people who would like to explore the possibilities of improving things like minimum wage, housing, health care, etc. The community is encouraged to get involved by organizing in their own communities and by striking on October 15th, 2021. As well as participating in capital boycotts, sit-ins, and walk-outs until the demands of the movement are acknowledged by the United States government.
    </p>
    <p>
      Important note: The October Labor Movement does not encourage or endorse Wildcat Strikes. Click here to learn more about what a strike is and the importance of unionizing. 
    </p>
      
  </div>
</section>

<style>

  .plan-section {
    position: relative;
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