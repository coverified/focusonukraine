<script>
	export let href, height;
</script>

<a
	class="twitter-timeline"
	data-lang="de"
	data-height={height}
	data-dnt="true"
	data-theme="light"
	{href}
/>

<svelte:head>
	<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
</svelte:head>
