<script>
	import AccountList from '$lib/components/AccountList.svelte';
	import TwitterEmbed from '$lib/components/TwitterEmbed.svelte';
	import GermanTwitterAccounts from '$lib/data/germanTwitterAccounts.json';
	import InternationalTwitterAccounts from '$lib/data/internationalTwitterAccounts.json';
</script>

<p class="intro">
	#FocusOnUkraine bündelt vertrauenswürdige Informationen zum Krieg in der Ukraine. Zur aktuellen
	Lage berichten anerkannte internationale und nationale Twitterstimmen.
</p>

<h2>Internationale Twitterstimmen</h2>
<div class="text-center" on:load={twttr.widgets.load()}>
	<TwitterEmbed
		href="https://twitter.com/DDAlliance_org/lists/1498308539399479304?ref_src=twsrc%5Etfw"
		height="500"
	/>
	<a href="aktuelles/internationale-twitterstimmen" title="Deutsche Twitterstimmen">
		alle anzeigen
	</a>
</div>
<AccountList twitterAccounts={InternationalTwitterAccounts} />

<h2>Deutsche Twitterstimmen</h2>
<div class="text-center" on:load={twttr.widgets.load()}>
	<TwitterEmbed
		href="https://twitter.com/DDAlliance_org/lists/1498306204338171904?ref_src=twsrc%5Etfw"
		height="500"
	/>
	<a href="aktuelles/deutsche-twitterstimmen" title="Deutsche Twitterstimmen"> alle anzeigen </a>
</div>

<AccountList twitterAccounts={GermanTwitterAccounts} />

<style lang="scss">
</style>
