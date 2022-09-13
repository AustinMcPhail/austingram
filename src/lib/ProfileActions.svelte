<script lang="ts">
	export let username = 'WhalePhail';
</script>

<div class="name">
	<p>
		{username}
	</p>
	<ul>
		<button>Message</button>
		<button>Follow</button>
		<button class="more">&bull; &bull; &bull;</button>
	</ul>
</div>

<style>
	.name {
		display: flex;
		flex-wrap: wrap;
		gap: var(--lg);
		align-items: center;
	}
	.name ul {
		display: flex;
		flex-wrap: wrap;
		align-items: center;
		gap: var(--sm);

		padding: 0;
	}
	.more {
		white-space: nowrap;
		word-break: keep-all;
	}
</style>
