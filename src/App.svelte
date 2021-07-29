<script>
	import page from 'page'
	
	import Nav from './sharedComponents/Nav.svelte'
	import Sock from './sharedComponents/Sock.svelte'
	import Footer from './sharedComponents/Footer.svelte'
	import Home from './Home/Home.svelte'
	import MutualAid from './MutualAid/MutualAid.svelte'
	import StrikeWithUs from './StrikeWithUs/StrikeWithUs.svelte'

	let component = Home

	page('', () => component = Home)
	page('/mutual-aid', () => component = MutualAid)
	page('/strike-with-us', () => component = StrikeWithUs)
	page('*', () => component = Home)
	page.start()

</script>

<main>
	<Nav />
	<svelte:component this={component} />
	<Sock navy={component = StrikeWithUs} />
	<Footer />
</main>
