<script>
  import Header from '../sharedComponents/Header.svelte'  
  import MissionAndGoals from './MissionAndGoals/MissionAndGoals.svelte';
  // import AboutDemandsSection from './AboutDemandsSection/AboutDemandsSection.svelte';
  import WhoWeAreSection from './WhoWeAreSection/WhoWeAreSection.svelte';
  import JoinSection from './JoinSection/JoinSection.svelte';
  import GetInTouchSection from './GetInTouchSection/GetInTouchSection.svelte';
</script>

<Header title='About Us <span class="emphasize">#WeAreThe<wbr>Movement</wbr></span>' image='/assets/images/gayatri-malhotra-bjaALmGB6qY-unsplash.jpeg' />
<WhoWeAreSection />
<MissionAndGoals />
<JoinSection />
<GetInTouchSection />
