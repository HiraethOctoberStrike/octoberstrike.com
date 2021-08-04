<script>
  import HeaderWImage from '../../sharedComponents/HeaderWImage.svelte'
  import { demands } from '../../copy.js'
</script>

<HeaderWImage 
  headerText='Join and support the strike'
  image='/assets/images/phil-desforges-PyCQPOvq404-unsplash.jpeg' >
  <ul>
    <div class='column'>
      {#each demands[0] as demand }
        <h4><li>{demand}</li></h4>
      {/each}
    </div>
    <div class='column'>
      {#each demands[1] as demand }
        <h4><li>{demand}</li></h4>
      {/each}
    </div>
  </ul>
</HeaderWImage>

<style>
  ul {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    padding: 0;
  }

  .column {
    flex: 1 1 50%;
  }

  h4 {
    margin: 0 50px 50px;
  }

  li {
    color: var(--white);
    list-style-type: square;
  }

  @media (max-width: 800px) {
    .column {
      flex: 1 1 100%;
    }
    
    h4 {
      margin-bottom: 30px
    }
  }

</style>