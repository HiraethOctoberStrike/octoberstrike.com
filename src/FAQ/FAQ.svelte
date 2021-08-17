<script>
  import Header from '../sharedComponents/Header.svelte'
  import DemandsSection from '../sharedComponents/DemandsSection.svelte'
  import TransparencySection from './TransparencySection/TransparencySection.svelte'
  import QuestionsSection from './QuestionsSection/QuestionsSection.svelte'
  import MoreQuestionsSection from './MoreQuestionsSection/MoreQuestionsSection.svelte'


  // google analytics
  gtag('config', 'G-XCYV4MQQL3', {
    'page_path': '/faq',
    'page_title': 'FAQ'
  })
</script>
<Header title='Frequently Asked Questions' />
<DemandsSection />
<!-- <TransparencySection /> -->
<QuestionsSection />
<MoreQuestionsSection />