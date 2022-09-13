<script lang="ts">
	import ProfileHead from '$lib/ProfileHead.svelte';
	import Space from '$lib/Space.svelte';
	export let stories: { id: string; title: string; imageUrl: string }[] = [
		{
			id: 'biking',
			title: 'Biking',
			imageUrl:
				'https://images.unsplash.com/photo-1528629297340-d1d466945dc5?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2722&q=80'
		}
	];
</script>

<section>
	<div class="container">
		<a href="/" class="story new"> ➕ </a>
		<p>New</p>
	</div>
	{#each stories as story}
		<div class="container">
			<a style={`--img: url('${story.imageUrl}');`} href={`/stories/${story.id}`} class="story">
				<span class="sr-only">{story.title}</span>
			</a>
			<p>{story.title}</p>
		</div>
	{/each}
</section>

<style>
	a {
		text-decoration: none;
	}

	section {
		display: flex;
		flex-wrap: none;
		overflow-x: auto;

		max-width: calc(100vw - 2 * var(--lg));
		margin: 0 auto;

		gap: var(--xl);
	}

	.container {
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	.story {
		display: block;
		width: clamp(50px, 25vw, 85px);
		height: clamp(50px, 25vw, 85px);

		border: solid 1px var(--dark);
		border-radius: 50%;

		background-image: var(--img);
		background-size: cover;
	}

	.new {
		display: flex;
		justify-content: center;
		align-items: center;
	}

	.sr-only {
		display: none;
	}
</style>
