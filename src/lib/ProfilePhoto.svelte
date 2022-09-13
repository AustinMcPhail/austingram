<script lang="ts">
	export let photo =
		'https://images.unsplash.com/photo-1552374196-c4e7ffc6e126?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1287&q=80';
	export let height = '';
	export let width = '';
</script>

<div
	class="container"
	style="{height ? `--height: ${height};` : ''}{width ? `--width: ${width};` : ''}"
>
	<div class="sizer">
		<div class="shaper">
			<img src={photo} alt="profile" />
		</div>
	</div>
</div>

<style>
	.container {
		flex-shrink: 0;
		display: flex;
		flex-direction: column;
		justify-content: center;
	}
	@media (min-width: 736px) {
		.container {
			flex-basis: 0px;
			flex-grow: 1;
			margin-right: 30px;
		}
	}

	.container > .sizer {
		display: block;
		margin-left: auto;
		margin-right: auto;
	}
	@media (max-width: 735px) {
		.container > .sizer {
			height: var(--height, calc(0.5 * 150px + 2px));
			width: var(--width, 77px);
		}
	}
	@media (min-width: 736px) {
		.container > .sizer {
			height: var(--height, calc(148px + 2px));
			width: var(--width, 150px);
		}
	}

	.container > .sizer > .shaper {
		background-color: var(--tiffany-blue);
		border-radius: 50%;
		box-sizing: border-box;
		height: 100%;
		margin: 0 auto;
		overflow: hidden;
		position: relative;
		width: 100%;
	}

	.container > .sizer > .shaper > img {
		width: 100%;
		height: 100%;
		object-fit: cover;
	}
</style>
