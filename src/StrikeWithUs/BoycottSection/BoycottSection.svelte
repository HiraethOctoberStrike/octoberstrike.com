<script>
  import { boycott } from '../../copy.js'
  import Card from '../../sharedComponents/Card.svelte'

</script>

<section class='boycott-section'>
  <h2>Boycott corporations and refrain from economic activity.</h2>
  <p>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Volutpat risus, nibh id egestas. Iaculis ultrices magna ac sed scelerisque blandit in ridiculus accumsan. Ac cursus diam posuere lectus. Pretium, quisque leo risus sed. Auctor penatibus non laoreet habitant sem.
  </p>
  <div class='boycott-cards'>
    {#each boycott as { title, snippet }, i }
      <Card {title} {snippet} navy={i % 2 == 0} small={true} />
    {/each}
  </div>
</section>

<style>
  p {
    margin-bottom: 30px;
    color: var(--black);
  }
 
  .boycott-cards {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    margin: -10px;
  }
</style>