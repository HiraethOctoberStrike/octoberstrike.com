<script>
  import { intersectionality } from '../../copy.JS'
</script>

<section class='intersectionality-section'>

  <h3>
    The fight for the rights of the working class is an intersectional issue.
  </h3>
  <div class='intersectionalities'>
    {#each intersectionality as { title, snippet }, i }
    <div class='intersectionality' class:darken={i ==1}>
      <h5>{title}</h5>
      <p>{snippet}</p>
    </div>
    {/each}
  </div>
</section>

<style>
  .intersectionality-section {
    background-color: var(--navy);
  }

  .intersectionalities {
    display: flex;
    flex-direction: row;
    margin: -10px;
  }

  .intersectionality {
    padding: 24px 18px;
    background-color: var(--white);
    box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.25);
    flex: 1 1;
    margin: 10px;
  }

  h5 {
    color: var(--black);
    margin-bottom: 24px;
  }

  p {
    color: var(--black);
  }

  @media (max-width: 1100px) {
    .intersectionalities {
      flex-wrap: wrap;
    }
    
    .intersectionality {
      flex: 1 0 30%;
    }
  }

  @media (max-width: 700px) {
    .intersectionality {
      flex: 1 1 auto;
    }
  }
</style>