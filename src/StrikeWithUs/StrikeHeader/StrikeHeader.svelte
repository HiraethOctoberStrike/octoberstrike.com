<script>
  import HeaderWImage from '../../sharedComponents/HeaderWImage.svelte'
  import { demands } from '../../copy.js'
</script>

<HeaderWImage 
  headerText='Join and support the strike'
  image='/assets/images/phil-desforges-PyCQPOvq404-unsplash.jpeg' >
  <ul>
    {#each demands as demand }
      <h4><li>{demand}</li></h4>
    {/each}
  </ul>
</HeaderWImage>

<style>
  ul {
    display: flex;
    flex-wrap: wrap;
    padding: 0;
  }

  h4 {
    flex: 1 1 30%;
    margin: 0 50px 50px;
  }

  li {
    color: var(--white);
    list-style-type: square;
  }

  @media (max-width: 800px) {
    h4 {
      margin-bottom: 20px
    }
  }

</style>