<script>
  import { boycott } from '../../copy.js'
  import Card from '../../sharedComponents/Card.svelte'

</script>

<section class='boycott-section'>
  <h2>Whether you’re able to strike or not, you can help us win this fight.</h2>
  <div class='boycott-cards'>
    {#each boycott as { title, snippet }, i }
      <Card {title} {snippet} navy={i % 2 == 0} small={true} />
    {/each}
  </div>
</section>

<style>
  h2 {
    margin-bottom: 40px;
  }
 
  .boycott-cards {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    margin: -10px;
  }
</style>