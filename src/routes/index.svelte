<script>
	import AccountList from '$lib/components/AccountList.svelte';
	import TwitterEmbed from '$lib/components/TwitterEmbed.svelte';
</script>

<h2>Deutsche Twitterstimmen</h2>
<div class="text-center">
	<TwitterEmbed
		href="https://twitter.com/zeitonline/lists/ukraine?ref_src=twsrc%5Etfw"
		height="500"
	/>
	<a href="/deutsche-twitterstimmen" title="Deutsche Twitterstimmen"> alle anzeigen </a>
</div>
<h2>Einzelne Accounts auswählen</h2>
<AccountList />

<style lang="scss">
</style>
