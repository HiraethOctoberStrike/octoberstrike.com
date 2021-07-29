<script>
  import HeaderWCTA from "../sharedComponents/HeaderWCTA.svelte";
  import Plan from "./Plan/Plan.svelte";
  import Safety from "./Safety/Safety.svelte";
  import Demands from "../sharedComponents/Demands.svelte";
  import MutualAid from "./MutualAidSection/MutualAidSection.svelte";
  import BoycottSection from "./BoycottSection/BoycottSection.svelte";

</script>

<HeaderWCTA 
  header='Join and support the strike'
  paragraph='Lorem ipsume dolor sit amet, consectetur adipiscing elit. Ornare duis lacus neque adipiscing aliquam molestie fermentum. Eget commodo quisque non, porta. In congue sociis donec vel laoreet in pharetra. Vitae habitant et.'
  buttonText='SHOW YOUR COMMITMENT BY SIGNING THE PETITION'
  buttonHref='http://chng.it/kNQvH8GXL5'
  smallText={true} />
<Demands large={true} />
<Plan />
<Safety />
<MutualAid />
<BoycottSection />
<style>

</style>