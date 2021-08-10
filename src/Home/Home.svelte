<script>
  import { demands } from '../copy.js'

  import HomeHeader from './HomeHeader/HomeHeader.svelte'
  import DemandsSection from '../sharedComponents/DemandsSection.svelte'
  import ChangeSection from './ChangeSection/ChangeSection.svelte'
  import IntersectionalitySection from './IntersectionalitySection/IntersectionalitySection.svelte'
  import WeWaitedSection from './WeWaitedSection/WeWaitedSection.svelte'

  // google analytics
  gtag('config', 'G-XCYV4MQQL3', {
    'page_path': '/home',
    'page_title': 'Home'
  })

</script>

<HomeHeader />
<DemandsSection {demands} />
<ChangeSection />
<IntersectionalitySection />
<WeWaitedSection />

