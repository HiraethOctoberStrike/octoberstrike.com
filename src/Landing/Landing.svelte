<script>
  import { faqDemands } from '../copy.js'
  import IntroSection from './IntroSection/IntroSection.svelte'
  import WhatToExpectSection from './WhatToExpectSection/WhatToExpectSection.svelte'
  import DemandsSection from '../sharedComponents/DemandsSection.svelte'
  import ThankYouSection from './ThankYouSection/ThankYouSection.svelte'

</script>

<IntroSection />
<DemandsSection demands={faqDemands} red />
<WhatToExpectSection />
<ThankYouSection/>
