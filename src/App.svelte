<script>
	import page from 'page'
	
	import Home from './Home/Home.svelte'

	let component = Home

	page('', () => component = Home)
	page('*', () => component = Home)
	page.start()

</script>

<main>
	<svelte:component this={component} />
</main>

<style>
	main {
		max-width: 240px;
	}


	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>