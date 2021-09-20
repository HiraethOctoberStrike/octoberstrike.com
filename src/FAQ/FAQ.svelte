<script>
  import { faqDemands } from '../copy'
  import FAQHeader from './FAQHeader/FAQHeader.svelte'
  import Demands from '../sharedComponents/DemandsSection.svelte'
  import TransparencySection from './TransparencySection/TransparencySection.svelte'
  import QuestionsSection from './QuestionsSection/QuestionsSection.svelte'
  import MoreQuestionsSection from './MoreQuestionsSection/MoreQuestionsSection.svelte'

</script>

<FAQHeader/>
<Demands demands={faqDemands} />
<TransparencySection />
<QuestionsSection />
<MoreQuestionsSection />
