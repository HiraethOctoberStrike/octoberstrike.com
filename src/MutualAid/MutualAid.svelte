<script>
  import MutualAidHeader from './MutualAidHeader/MutualAidHeader.svelte'
  import OrganizationsSection from './OrganizationsSection/OrganizationsSection.svelte'
  import WhatIsMutualAidSection from './WhatIsMutualAidSection/WhatIsMutualAidSection.svelte'
  
  // google analytics
  gtag('config', 'G-XCYV4MQQL3', {
    'page_path': '/mutual-aid',
    'page_title': 'Mutual Aid'
  })

</script>

<MutualAidHeader />
<WhatIsMutualAidSection />
<OrganizationsSection />
