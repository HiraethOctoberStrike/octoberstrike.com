<script>
  import Button from '../sharedComponents/Button.svelte'
</script>

<section class='landing-page'>
  <div class='h1-container'>
    <h1>Labor Movement X</h1>
  </div>
  <img src='/assets/images/LMX_Logo_White-8.png' alt='labor movement x logo' />
  <h5>
    You seem to have stumbled on the new website for the October Resistance!
  </h5>
  <p>
    Whether you are a member of the working class, an activist, a social media connoisseur, or just a concerned citizen, the members at Labor Movement X welcome you with open arms. No matter where you’re from, we hope that this statement reaches you in good conscience.
  </p>
  <h6>Why are we called Labor Movement X?</h6>
  <p>
    Originally, this event was marketed exclusively as a strike. While this movement is largely centered around a general economic strike, we want to be sure that the world knows that this is not just a strike. This is a nationwide campaign that will fight for the rights of all working class people, by whatever means necessary. There are multiple ways to participate in this movement from: striking, to boycotting, picketing, participating in sit-ins, peaceful protesting, outreach, and many more. Because of this, we decided to change the name of the event to the October Resistance, and the name of the movement as a whole to Labor Movement X. X for 10. 10th month, 10 days, 10 demands. 
  </p>

  <div class='button-container'>
    <Button text='SEE OUR DEMANDS' href='/strike-with-us' secondary />
  </div>

  <h6>What should you expect in the coming days? </h6>

  <p>
    This is a list of all information that will be released in the next week.
  </p>

  <p class='italicize'>Thursday, August 5th:</p>
  <p>FAQ</p>

  <p class='italicize'>Friday, August 6th:</p>
  <p>Declaration of demands</p>

  <p class='italicize'>Sunday, August 8th:</p>
  <p>Supporting essays for each demand</p>

  <p class='italicize'>Monday, August 9th:</p>
  <p>
    Union resource guide and action plan<br>
    Mutual aid resource guide and action plan<br>
    Public outreach guide<br>
    Complete action plan for the October Resistance<br>
    Statewide canvassing and event planning
  </p>

  <p>
    We thank you for your patience and support during this time. We are thrilled to be facilitating this movement, and know that all of you are ready and excited to participate. If you have any further inquiries, please feel free to reach out to our Public Relations team at <a href='mailto: labormovementxPR@gmail.com'>labormovementxPR@gmail.com</a>
  </p>

  <p>
    Thank you, 
  </p>

  <p class='italicize'>
    Alex Deval<br>
    Public Relations Chair 
  </p>


  <div class='button-container'>
    <Button text='CONTINUE TO SITE' href='/home' tertiary />
  </div>
</section>

<style>
  .landing-page {
    display: flex;
    flex-direction: column;
  }

  .h1-container {
    position: relative;
    background-color: var(--white);
    padding: 30px;
    box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.25);
    display: inline-block;
  }

  .landing-page {
    background-color: var(--navy);
  }

  img {
    width: 158px;
    margin: 60px 0 12px;
  }

  h5 {
    margin-bottom: 36px;
  }

  h6 {
    color: var(--white);
  }

  p {
    color: var(--white);
    margin-bottom: 24px;
  }

  .italicize {
    margin-bottom: 0;
  }

  .button-container {
    margin: 12px 0 48px;
    align-self: flex-start;
  }

  .button-container:last-child {
    margin-top: 60px;
  }

</style>