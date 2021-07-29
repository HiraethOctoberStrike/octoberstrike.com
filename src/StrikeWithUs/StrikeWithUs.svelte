<script>
  import HeaderWCTA from "../sharedComponents/HeaderWCTA.svelte";
  import PlanSection from "./PlanSection/PlanSection.svelte";
  import SafetySection from "./SafetySection/SafetySection.svelte";
  import DemandsSection from "../sharedComponents/Demands.svelte";
  import MutualAidSection from "./MutualAidSection/MutualAidSection.svelte";
  import BoycottSection from "./BoycottSection/BoycottSection.svelte";
  import SupportSection from "./SupportSection/SupportSection.svelte";
  import ResourcesSection from "./ResourcesSection/ResourcesSection.svelte";
</script>

<HeaderWCTA 
  header='Join and support the strike'
  paragraph='Lorem ipsume dolor sit amet, consectetur adipiscing elit. Ornare duis lacus neque adipiscing aliquam molestie fermentum. Eget commodo quisque non, porta. In congue sociis donec vel laoreet in pharetra. Vitae habitant et.'
  buttonText='SHOW YOUR COMMITMENT BY SIGNING THE PETITION'
  buttonHref='http://chng.it/kNQvH8GXL5'
  smallText={true} />
<DemandsSection large={true} />
<PlanSection />
<SafetySection />
<MutualAidSection />
<BoycottSection />
<SupportSection />
<ResourcesSection />

<style>

</style>