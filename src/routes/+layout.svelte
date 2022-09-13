<script>
	import Header from '$lib/Header.svelte';
	import '$lib/theme.css';
</script>

<Header messageCount={1} />
<main>
	<slot />
</main>

<style>
	main {
		padding: 30px 20px 0;
	}
</style>
