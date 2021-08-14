<script>
  import HeaderWContent from '../../sharedComponents/HeaderWContent.svelte'
  import Button from '../../sharedComponents/Button.svelte'
  import { mutualAidLinks } from '../../copy.js'
</script>

<HeaderWContent 
  headerText='Support yourself and your community'
  image='/assets/images/robert-bye-4hcpIbqQM8c-unsplash.jpeg' >
  <div class='mutual-aid-links'>
    {#each mutualAidLinks as { text, href } }
      <div class='button-container'>
        <Button {text} {href} red large external/>
      </div>
    {/each}
  </div>
</HeaderWContent>

<style>
  .mutual-aid-links {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    margin: 0 -30px;
  }

  .button-container {
    display: flex;
    flex: 1 1 50%;
    margin-bottom: 20px;
  }

  @media (max-width: 500px) {
    .mutual-aid-links {
      margin: 0 -16px;
    }
  }
</style>