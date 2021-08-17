<script>
	import page from 'page'
	
	import Nav from './Nav/Nav.svelte'
	import Sock from './Sock/Sock.svelte'
	import Footer from './Footer/Footer.svelte'
	import Landing from './Landing/Landing.svelte'
	import Home from './Home/Home.svelte'
	// import MutualAid from './MutualAid/MutualAid.svelte'
	import About from './About/About.svelte'
	import JoinTheMovement from './JoinTheMovement/JoinTheMovement.svelte'
	import FAQ from './FAQ/FAQ.svelte'

	let component = Landing
	page('', () => component = Landing)
	page('/home', () => component = Home)
	// page('/mutual-aid', () => component = MutualAid)
	page('/about', () => component = About)
	page('/strike-with-us', () => component = JoinTheMovement)
	page('/faq', () => component = FAQ)
	page('*', () => component = Landing)
	page.start()
	page.exit('*', (ctx, next) => {
  	window.scroll(0, 0)
 	 next()
	})

</script>

<main>
	<Nav />
	<svelte:component this={component} />
	{#if component !== Landing}
		<Sock
			red={component === FAQ}
			navy={component === JoinTheMovement} 
			joinTheMovement={component !== JoinTheMovement}/>
	{/if}
	<Footer />
</main>
