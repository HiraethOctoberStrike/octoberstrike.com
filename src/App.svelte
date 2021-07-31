<script>
	import page from 'page'
	
	import Nav from './Nav/Nav.svelte'
	import Sock from './Sock/Sock.svelte'
	import Footer from './Footer/Footer.svelte'
	import Home from './Home/Home.svelte'
	import MutualAid from './MutualAid/MutualAid.svelte'
	import StrikeWithUs from './StrikeWithUs/StrikeWithUs.svelte'

	let component = Home
	page('', () => component = Home)
	page('/mutual-aid', () => component = MutualAid)
	page('/strike-with-us', () => component = StrikeWithUs)
	page('*', () => component = Home)
	page.start()
	page.exit('*', (ctx, next) => {
  	window.scroll(0, 0)
 	 next()
	})

</script>

<main>
	<Nav />
	<svelte:component this={component} />
	<Sock navy={component === StrikeWithUs} />
	<Footer />
</main>
