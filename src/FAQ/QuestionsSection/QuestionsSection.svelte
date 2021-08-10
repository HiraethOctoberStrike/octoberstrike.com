<script>
  import { faqQuestions } from '../../copy.js'
  import DropDownCard from '../../sharedComponents/DropDownCard.svelte'
  import Section from '../../sharedComponents/Section.svelte'
</script>

<Section>
  <h3>
    There may be subcategories of questions but I’m not sure. 
  </h3>
  <div class='question-group'>
    {#each faqQuestions as { title, body } }
      <DropDownCard {title} {body} />
    {/each}
  </div>
  <h3>
    There may be subcategories of questions but I’m not sure. 
  </h3>
  <div class='question-group'>
    {#each faqQuestions as { title, body } }
      <DropDownCard {title} {body} />
    {/each}
  </div>
</Section>

<style>
  h3 {
    color: var(--black);
  }

  .question-group {
    margin-bottom: 70px;
  }

  .question-group:last-child {
    margin-bottom: 0;
  }
</style>