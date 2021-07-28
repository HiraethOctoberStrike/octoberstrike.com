<script>
	import page from 'page'
	
	import Nav from './sharedComponents/Nav.svelte'
	import Sock from './sharedComponents/Sock.svelte'
	import Footer from './sharedComponents/Footer.svelte'
	import About from './About/About.svelte'
	import Home from './Home/Home.svelte'
	import GetInvolved from './GetInvolved/GetInvolved.svelte'
	import MutualAid from './MutualAid/MutualAid.svelte'
	import FAQ from './FAQ/FAQ.svelte'
	import StrikeWithUs from './StrikeWithUs/StrikeWithUs.svelte'

	let component = Home

	page('', () => component = Home)
	page('/about', () => component = About)
	page('/get-involved', () => component = GetInvolved)
	page('/mutual-aid', () => component = MutualAid)
	page('/faq', () => component = FAQ)
	page('/strike-with-us', () => component = StrikeWithUs)
	page('*', () => component = Home)
	page.start()

</script>

<main>
	<Nav />
	<svelte:component this={component} />
	<Sock />
	<Footer />
</main>
