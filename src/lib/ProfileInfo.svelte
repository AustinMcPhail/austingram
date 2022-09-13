<script lang="ts">
	export let name = 'Austin McPhail';
	export let pronouns = 'he/him';
	export let bio = 'Hello World';
	export let website = 'https://squirdle.xyz/';
</script>

<p class="name">
	{name} <span>{pronouns}</span>
</p>
<p class="bio">
	{bio}
</p>
<a class="website" href={website} rel="noopener noreferrer" target="_blank">
	{website}
</a>

<style>
	p.name {
		font-weight: var(--thicc);
		display: flex;
		gap: var(--sm);
	}
	p.name span {
		font-weight: var(--thinn);
		opacity: 0.75;
	}

	a.website {
		position: relative;
		display: inline-block;
		font-weight: var(--thicc);
		color: var(--dark);
		text-decoration: none;
	}
	a.website::after {
		position: absolute;
		left: 0;
		bottom: 0;
		content: '';
		width: 0;
		height: 2px;
		background: var(--dark);
		transition: width 0.25s ease;
	}
	a.website:hover::after {
		width: 100%;
	}
</style>
