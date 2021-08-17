<script>
  import Section from '../../sharedComponents/Section.svelte'
</script>

<Section>
  <div class='who-we-are-section'>
    <div class='content'>
      <h2>
        Labor Movement X is a diverse group of <span class='emphasize'>working class</span> adults.
      </h2>
      <h6> We have come together to demand legislative and corporate change, for the benefit of all who live and work in this country.</h6>
    </div>
    <img src='assets/images/toa-heftiba-6bKpHAun4d8-unsplash.jpeg' />
  </div>
</Section>

<style>
  .who-we-are-section {
    display: flex;
    flex-direction: row;
    align-items: center;
  }

  img {
    margin-left: 50px;
    display: flex;
    flex: 0 2 50%;
    max-height: 500px;
    width: 100%;
    object-fit: contain;
  }

  .content {
    display: flex;
    flex-direction: column;
    flex: 1 0 50%;
    flex-shrink: 1;
  }

  h6 {
    margin-top: 40px;
    color: var(--dark-grey);
  }
 
  @media (max-width: 1000px) {
    .who-we-are-section {
      flex-direction: column;
    }

    img {
      margin: 0 0 50px;
      flex: unset;
    }

    .content {
      flex: unset;
    } 
  }
</style>