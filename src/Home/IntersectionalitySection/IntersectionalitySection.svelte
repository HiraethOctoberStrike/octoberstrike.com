<script>
  import { intersectionality } from '../../copy.js'
  import Section from '../../sharedComponents/Section.svelte'
  import Card from '../../sharedComponents/Card.svelte'
</script>

<Section navy>
  <h3>
    The fight for the rights of the working class is an intersectional issue.
  </h3>
  <div class='intersectionalities'>
    {#each intersectionality as { title, snippet }, i }
      <Card {title} peach small >
        <p>{snippet}</p>
      </Card>
    {/each}
  </div>
</Section>

<style>
  .intersectionalities {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    margin: -10px;
  }

  p {
    color: var(--black);
  }
</style>