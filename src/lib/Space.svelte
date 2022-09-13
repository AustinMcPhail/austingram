<script lang="ts">
	export let size: 'xs' | 'sm' | 'md' | 'lg' | 'xl' = 'md';
</script>

<hr class={size} />

<style>
	hr {
		border: none;
		height: 0px;
	}

	.xs {
		height: var(--xs);
	}

	.sm {
		height: var(--sm);
	}

	.md {
		height: var(--md);
	}

	.lg {
		height: var(--lg);
	}

	.xl {
		height: var(--xl);
	}
</style>
