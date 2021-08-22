<script>
  import PlanSection from "./PlanSection/PlanSection.svelte";
  import SafetySection from "./SafetySection/SafetySection.svelte";
  import MutualAidSection from "./MutualAidSection/MutualAidSection.svelte";
  import BoycottSection from "./BoycottSection/BoycottSection.svelte";
  import SupportSection from "./SupportSection/SupportSection.svelte";
  // import ResourcesSection from "./ResourcesSection/ResourcesSection.svelte";
  import JoinTheMovementHeader from "./JoinTheMovementHeader/JoinTheMovementHeader.svelte";

  // google analytics
  gtag('config', 'G-XCYV4MQQL3', {
    'page_path': '/join-the-movement',
    'page_title': 'Join the Movement'
  })

</script>

<JoinTheMovementHeader />
<PlanSection />
<BoycottSection />
<SafetySection />
<MutualAidSection />
<SupportSection />
<!-- <ResourcesSection /> -->