<script>
  import DemandsSection from '../sharedComponents/DemandsSection.svelte'
  import QuestionsSection from './QuestionsSection/QuestionsSection.svelte'

  // google analytics
  gtag('config', 'G-XCYV4MQQL3', {
    'page_path': '/faq',
    'page_title': 'FAQ'
  })
</script>

<DemandsSection />
<QuestionsSection />