<script>
	import page from 'page'
	
	import Nav from './Nav/Nav.svelte'
	import Sock from './Sock/Sock.svelte'
	import Footer from './Footer/Footer.svelte'
	import Home from './Home/Home.svelte'
	import MutualAid from './MutualAid/MutualAid.svelte'
	import About from './About/About.svelte'
	import JoinTheMovement from './JoinTheMovement/JoinTheMovement.svelte'
	import FAQ from './FAQ/FAQ.svelte'

	let component = Home
	page('', () => component = Home)
	page('/mutual-aid', () => component = MutualAid)
	page('/about', () => component = About)
	page('/join-the-movement', () => component = JoinTheMovement)
	page('/faq', () => component = FAQ)
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
	{#if component !== Home}
		<Sock
			red={component === FAQ}
			navy={component === JoinTheMovement} 
			joinTheMovement={component !== JoinTheMovement}/>
	{/if}
	<Footer />
</main>
