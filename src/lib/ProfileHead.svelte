<script lang="ts">
	import Space from '$lib/Space.svelte';

	import ProfileActions from './ProfileActions.svelte';

	import ProfileInfo from './ProfileInfo.svelte';

	import ProfilePhoto from './ProfilePhoto.svelte';
	import ProfileStats from './ProfileStats.svelte';

	export let username = 'WhalePhail';
	export let name = 'Austin McPhail';
	export let pronouns = 'he/him';
	export let bio = 'Hello World';
	export let website = 'https://squirdle.xyz/';
	export let photo =
		'https://images.unsplash.com/photo-1552374196-c4e7ffc6e126?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1287&q=80';
</script>

<section>
	<ProfilePhoto {photo} />
	<div class="info">
		<ProfileActions {username} />
		<ProfileStats />
		<Space />
		<ProfileInfo {name} {pronouns} {website} {bio} />
	</div>
</section>

<style>
	section {
		align-items: stretch;
		display: flex;
		flex-direction: row;
		position: relative;

		gap: var(--lg);
	}

	.info {
		flex-basis: 30px;
		flex-grow: 2;
	}
</style>
