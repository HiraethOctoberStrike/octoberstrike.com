<script>
  import HeaderWImage from '../../sharedComponents/HeaderWImage.svelte'
  import Button from '../../sharedComponents/Button.svelte'
  import { mutualAidLinks } from '../../copy.js'
</script>

<HeaderWImage 
  headerText='Join and support the strike'
  image='https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse1.mm.bing.net%2Fth%3Fid%3DOIP.MB8pq1-VyWEzA4NLbhy95wHaFi%26pid%3DApi&f=1' >
  <div class='mutual-aid-links'>
    {#each mutualAidLinks as { text, href } }
      <div class='button-container'>
        <Button {text} {href} tertiary large />
      </div>
    {/each}
  </div>
</HeaderWImage>

<style>
  .mutual-aid-links {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    margin: 0 -30px;
  }

  .button-container {
    display: flex;
    flex: 1 1 450px;
    margin-bottom: 20px;
  }

  @media (max-width: 500px) {
    .mutual-aid-links {
      margin: 0 -16px;
    }
  }
</style>