<script>
  import Section from '../../sharedComponents/Section.svelte'
  import Button from '../../sharedComponents/Button.svelte'

</script>

<Section narrow>
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
    <Button text='CONTINUE TO SITE' href='/home' red />
  </div>
</Section>


<style>
  .button-container {
    margin-top: 12px;
    align-self: flex-start;
  }

  p {
    margin-bottom: 30px
  }

  p:first-child {
    margin-top: -55px;
  }
</style>