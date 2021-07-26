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
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>