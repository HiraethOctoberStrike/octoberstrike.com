<script>
  import { faqQuestions } from '../../copy.js'
  import DropDownCard from '../../sharedComponents/DropDownCard.svelte'
  import Section from '../../sharedComponents/Section.svelte'
</script>

<Section>
  <div class='question-group'>
    {#each faqQuestions as { title, body } }
      <DropDownCard {title} {body} />
    {/each}
  </div>
</Section>

<style>
  .question-group {
    margin-bottom: 70px;
  }

  .question-group:last-child {
    margin-bottom: 0;
  }
</style>