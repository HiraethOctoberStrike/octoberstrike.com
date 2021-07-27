<script>
	import page from 'page'
	
	import Home from './Home/Home.svelte'
	import StrikeWithUs from './StrikeWithUs/StrikeWithUs.svelte'

	let component = Home

	page('', () => component = Home)
	page('/strike-with-us', () => component = StrikeWithUs)
	page('/about', () => component = StrikeWithUs)
	page('/get-involved', () => component = StrikeWithUs)
	page('/faq', () => component = StrikeWithUs)
	page('*', () => component = Home)
	page.start()

</script>

<main>
	<svelte:component this={component} />
</main>

<style>
	@media (min-width: 640px) {
		
	}
</style>