<section class='plan-section'>
  <img src='assets/images/skyler-gerald-qADoh-Ag7s0-unsplash.jpeg' />
  <div class='plan-content'>
    <h2>We've got a plan:</h2>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ipsum, a ac est pulvinar lacus diam. Lacus, etiam massa adipiscing dui justo massa. Sapien, neque ultricies vel proin ipsum laoreet. Diam sed commodo aliquet ac ipsum pellentesque cras convallis enim. Vestibulum gravida libero eget magna arcu. Non facilisi semper augue elementum mauris quam placerat. Pulvinar scelerisque auctor orci, ultrices in. Tellus nulla metus eu proin pulvinar aliquam pulvinar odio. Eget nec porttitor velit.
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

  h2 {
    margin-bottom: 20px;
  }
  
  p {
    color: var(--dark-grey);
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