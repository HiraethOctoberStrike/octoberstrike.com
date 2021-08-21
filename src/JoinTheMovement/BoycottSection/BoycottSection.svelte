<script>
  import Card from '../../sharedComponents/Card.svelte'
  import SocialLinks from '../../sharedComponents/SocialLinks.svelte'
  import Button from '../../sharedComponents/Button.svelte'
  import Section from '../../sharedComponents/Section.svelte'

</script>

<Section navy>
  <h2>Participate in The Movement for workers rights</h2>
  <div class='boycott-cards'>
      <Card title='Unionize & Strike (peacefully)' peach small>
        <p>Start connecting and organizing with your fellow workers. Join a union representing your job and follow their guidance.</p>
        <div class='button-container'>
          <Button 
            text='FIND A UNION' 
            href='https://olmsapps.dol.gov/query/getOrgQry.do' 
            white external />
        </div>
      </Card>
      <Card title='Get Loud & Share Your Story' small>
        <p>Get loud on social media and spread the word! Right now, reaching people across the world is essental to making October as successful as possible.</p>
        <div class='social-links-container'>
          <SocialLinks />
        </div>
      </Card>
      <Card title='Participate in October’s events' peach small>
        <p>Put your money where your mouth is and participate in the October capital strike boycotts to make your voice heard with your money. Boycott big businesses like Amazon, Walmart, and Target to shop small instead.</p>
      </Card>
      <Card title='Organize in your state'  small>
        <p>Get involved within your community to organize.</p>
        <div class='button-container'>
          <Button 
          text='REQUEST TO JOIN DISCORD' 
          href='https://discord.gg/87k2EY4aRx' 
          white external />
        </div>
      </Card>
      <Card title='Get Involved with Mutual Aid' peach small>
        <p>Support your community and those at risk by donating to mutual aid funds.</p>
        <div class='button-container'>
          <Button 
          text='EXPLORE MUTUAL AID' 
          href='/mutual-aid ' 
          white />
        </div>
      </Card>
      <Card title='Write Your State Officials' small>
        <p>Text POKDHC to 50409</p>
        <div class='button-container'>
          <Button 
          text='TWEET WITH RESISTBOT' 
          href='https://twitter.com/openletterbot/status/1428096782152527877' 
          white
          external />
        </div>
      </Card>
  </div>
</Section>

<style>
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
    margin-left: -20px;
  }
</style>