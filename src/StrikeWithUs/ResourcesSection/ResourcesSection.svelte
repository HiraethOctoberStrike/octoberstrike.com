<script>
  import { resources } from '../../copy.js'
  import Button from '../../sharedComponents/Button.svelte'
  import Section from '../../sharedComponents/Section.svelte'
</script>

<Section narrower>
  <h2>Other Resources</h2>
  <div class='resources-container'>
    {#each resources as { text, href } }
      <div class='button-container'>
        <Button {text} {href} white />
      </div>
    {/each}
  </div>
</Section>

<style>
  h2 {
    margin-bottom: 40px
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
  
  @media (max-width: 1100px) {
    .button-container {
      flex: 0 1 250px;
    }
  }

  @media (max-width: 500px) {
    .resources-container {
      margin: 0 -16px;
    }
  }
</style>