<script>
	import AccountList from '$lib/components/AccountList.svelte';
	import TwitterEmbed from '$lib/components/TwitterEmbed.svelte';
	import GermanTwitterAccounts from '$lib/data/germanTwitterAccounts.json';
	import InternationalTwitterAccounts from '$lib/data/internationalTwitterAccounts.json';
</script>

<h2>Deutsche Twitterstimmen</h2>
<div class="text-center" on:load={twttr.widgets.load()}>
	<TwitterEmbed
		href="https://twitter.com/zeitonline/lists/ukraine?ref_src=twsrc%5Etfw"
		height="500"
	/>
	<a href="aktuelles/deutsche-twitterstimmen" title="Deutsche Twitterstimmen"> alle anzeigen </a>
</div>
<AccountList twitterAccounts={GermanTwitterAccounts}/>
<h2>Internationale Twitterstimmen</h2>
<div class="text-center" on:load={twttr.widgets.load()}>
	<TwitterEmbed
		href="https://twitter.com/zeitonline/lists/ukraine?ref_src=twsrc%5Etfw"
		height="500"
	/>
	<a href="aktuelles/internationale-twitterstimmen" title="Deutsche Twitterstimmen"> alle anzeigen </a>
</div>

<AccountList twitterAccounts={InternationalTwitterAccounts} />

<style lang="scss">
</style>
