<script lang="ts">
	export let posts = 0;
	export let followers = 0;
	export let following = 0;
</script>

<ul>
	<li><span>{posts}</span> <span class="metric">posts</span></li>
	<li><span>{followers}</span> <span class="metric">followers</span></li>
	<li><span>{following}</span> <span class="metric">following</span></li>
</ul>

<style>
	ul {
		list-style: none;
		padding: 0;
		margin: 0;

		display: flex;
		flex-wrap: wrap;
		align-items: center;
		gap: var(--lg);
	}

	li > span {
		font-weight: var(--normal);
	}
	.metric {
		font-weight: var(--thinnn);
	}
</style>
