<script>
  import HeaderWImage from '../../sharedComponents/HeaderWImage.svelte'
  import { demands } from '../../copy.js'
</script>

<HeaderWImage 
  headerText='Join and support the strike'
  image='https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse1.mm.bing.net%2Fth%3Fid%3DOIP.MB8pq1-VyWEzA4NLbhy95wHaFi%26pid%3DApi&f=1' >
  <ul>
    {#each demands as { title } }
    <h3><li>{title}</li></h3>
    {/each}
  </ul>
</HeaderWImage>

<style>
  ul {
    display: flex;
    flex-wrap: wrap;
    padding: 0;
  }

  h3 {
    flex: 1 1 350px;
    margin: 0 50px 50px;
  }

  li {
    color: var(--white);
    list-style-type: square;
  }

  @media (max-width: 500px) {
    li {
      margin-bottom: 20px
    }
  }

</style>