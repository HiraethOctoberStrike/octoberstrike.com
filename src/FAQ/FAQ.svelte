<script>
  import FAQHeader from './FAQHeader/FAQHeader.svelte'
  import TransparencySection from './TransparencySection/TransparencySection.svelte'
  import QuestionsSection from './QuestionsSection/QuestionsSection.svelte'
  import MoreQuestionsSection from './MoreQuestionsSection/MoreQuestionsSection.svelte'


  // google analytics
  gtag('config', 'G-XCYV4MQQL3', {
    'page_path': '/faq',
    'page_title': 'FAQ'
  })
</script>
<FAQHeader/>
<TransparencySection />
<QuestionsSection />
<MoreQuestionsSection />