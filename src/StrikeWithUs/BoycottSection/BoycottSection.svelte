<script>
  import Card from '../../sharedComponents/Card.svelte'
  import SocialLinks from '../../sharedComponents/SocialLinks.svelte'
  import Button from '../../sharedComponents/Button.svelte'

</script>

<section class='boycott-section'>
  <h2>Whether you’re able to strike or not, you can help us win this fight.</h2>
  <div class='boycott-cards'>
      <Card title='Unionize & Strike (peacefully)' peach small>
        <p>Start connecting and organizing with your fellow workers. Join a union representing your job and follow their guidance.</p>
        <div class='button-container'>
          <Button 
            text='FIND A UNION' 
            href='https://olmsapps.dol.gov/query/getOrgQry.do' 
            secondary external />
        </div>
      </Card>
      <Card title='Get Loud & Share Your Story' small>
        <p>GGet loud on social media and spread the word! Right now, reaching people across the world is essental to making October as successful as possible.</p>
        <div class='social-links-container'>
          <SocialLinks />
        </div>
      </Card>
      <Card title='Boycott With Us' peach small>
        <p>Put your money where your mouth is and participate in the October capital strike boycotts to make your voice heard with your money. Boycott big businesses like Amazon, Walmart, and Target to shop small instead.</p>
      </Card>
      <!-- TODO: GET LINK FOR DISCORD -->
      <Card title='Become a State Coordinator'  small>
        <p>Get involved within your community to organize.</p>
        <div class='button-container'>
          <Button 
          text='REQUEST TO JOIN DISCORD' 
          href='#' 
          secondary external />
        </div>
      </Card>
      <!-- TODO: GET LINK FOR DISCORD -->
      <Card title='Get Involved with Mutual Aid' peach small>
        <p>Support your community and those at risk by donating to mutual aid funds.</p>
        <div class='button-container'>
          <Button 
          text='REQUEST TO JOIN DISCORD' 
          href='#' 
          secondary external />
        </div>
      </Card>
      <!-- TODO: GET LINK FOR TEMPLATE -->
      <Card title='Write Your State Officials' small>
        <p>Make your voice heard and ontact your state officials about our demands. </p>
        <div class='button-container'>
          <Button 
          text='DOWNLOAD TEMPLATE' 
          href='#' 
          secondary external />
        </div>
      </Card>
  </div>
</section>

<style>
  .boycott-section {
    background-color: var(--navy);
  }

  h2 {
    margin-bottom: 40px;
    color: var(--white);
  }
 
  .boycott-cards {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    margin: -10px;
  }

  .social-links-container {
    margin-top: 14px;
  }

  .button-container {
    display: flex;
    margin-top: 14px;
    max-width: 250px;
    margin-left: -20px;
  }

  @media (max-width: 500px) {
    .button-container {
      max-width: 180px;
    }
  }
</style>