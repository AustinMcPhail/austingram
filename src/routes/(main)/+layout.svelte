<script>
	import ProfileHead from '$lib/ProfileHead.svelte';
	import SecondaryNav from '$lib/SecondaryNav.svelte';
	import Space from '$lib/Space.svelte';
	import Stories from '$lib/Stories.svelte';
</script>

<ProfileHead />
<Space size="lg" />
<Stories />
<Space size="lg" />
<SecondaryNav>
	<slot />
</SecondaryNav>
