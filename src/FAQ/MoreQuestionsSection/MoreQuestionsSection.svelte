<script>
  import SocialLinks from '../../sharedComponents/SocialLinks.svelte'
  import Section from '../../sharedComponents/Section.svelte'
</script>

<Section>
  <h3>
    Have more questions?
  </h3>
  <h4>
    Reach out to us on social media.
  </h4>
  <SocialLinks/>
  <a class='email' href='mailto: LaborMovementX@gmail.com'>LaborMovementX@gmail.com</a>
</Section>

<style>
  h3 {
    color: var(--black);
  }

  h4 {
    margin-bottom: 20px;
    font-weight: 400;
  }

  a {
    padding-top: 40px;
  }
</style>