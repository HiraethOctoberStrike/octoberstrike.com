<script>
  import { faqDemands } from '../copy.js'
  import IntroSection from './IntroSection/IntroSection.svelte'
  import WhatToExpectSection from './WhatToExpectSection/WhatToExpectSection.svelte'
  import DemandsSection from '../sharedComponents/DemandsSection.svelte'
  import ThankYouSection from './ThankYouSection/ThankYouSection.svelte'

  // google analytics
  gtag('config', 'G-XCYV4MQQL3', {
    'page_path': '/',
    'page_title': 'Landing'
  })
</script>

<IntroSection />
<DemandsSection demands={faqDemands} red />
<WhatToExpectSection />
<ThankYouSection/>
