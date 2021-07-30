<script>
  import { resources } from '../../copy.js'
  import Button from '../../sharedComponents/Button.svelte'
</script>

<section class='resources-section'>
  <h2>Other Resources</h2>
  <div class='resources-container'>
    {#each resources as { text, href } }
      <div class='button-container'>
        <Button {text} {href} secondary={true} />
      </div>
    {/each}
  </div>
</section>

<style>

  h2 {
    margin-bottom: 40px
  }

  .resources-section {
    padding: 60px 290px;
  }

  .resources-container {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    margin: 0 -30px;
  }

  .button-container {
    display: flex;
    flex: 1 1 350px;
  }

  @media (max-width: 1300px) {
    .resources-section {
      padding: 60px 200px;
    }
  }
  
  @media (max-width: 1100px) {
    .resources-section {
      padding: 60px 160px;
    }
    
    .button-container {
      flex: 0 1 250px;
    }
  }

  @media (max-width: 900px) {
    .resources-section {
      padding: 60px 100px;
    }

  }
  
  @media (max-width: 900px) {
    .resources-section {
      padding: 60px 40px;
    }
  }

  @media (max-width: 500px) {
    .resources-container {
      margin: 0 -16px;
    }
  }
</style>