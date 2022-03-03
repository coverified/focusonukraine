<script>
	import factsforfriendslogo from '$lib/assets/factsforfriendslogo.png';
	const endpoint = 'https://cms.factsforfriends.de/facts?tags_contains=ukraine&_sort=date:DESC';
	
	const getData = async () => {
		const response = await fetch(endpoint);
		const result = await response.json();
		return result;
	};

	let promise = getData();
</script>

<h2>Fake vs. Fakt</h2>
<p>
	Facts for Friends macht Faktencheck verständlich und alltagstauglich. Nach dem Motto
	#ErzählMirKeineMärchen, liefern sie die besseren Argumente gegen Desinformationen und
	Verschwörungen.
</p>
<div class="height">
	{#await promise then data}
		{#each data as item}
			<img src={item.image_url} alt={item.headline} />
			<h2>{item.headline}</h2>
			<p>{item.snack}</p>
			<a
				href={`https://factsforfriends.de/fact/${item.id}`}
				rel="noopener"
				target="_blank"
				title="Mehr erfahren"
				class="fact-link"
			>
				Mehr erfahren
			</a>
		{/each}
	{/await}
</div>
<a class="factforfriends-link" href="https://factsforfriends.de/" title="Facts for Friends" rel="noopener" target="_blank">
	<img src={factsforfriendslogo} alt="FactsforFriends" />factsforfriends.de
</a>

<style lang="scss">
	.height {
		max-height: 25rem;
		overflow: auto;
		padding: 0 12px 21px 12px;
		border: 1px solid var(--border-color);

		h2 {
			margin-top: 0rem;
		}

		img {
			width: calc(100% + 24px);
			height: 174px;
			object-fit: cover;
			margin-bottom: 1rem;
			margin-right: -12px;
			margin-left: -12px;
		}

		.fact-link {
			margin-bottom: 2rem;
			display: block;
		}
	}

	.factforfriends-link {
		font-size: 1.25rem;
		display: block;
		margin-top: 1rem;
	}

	@media (min-width: 768px) {
		.height {
			max-height: 40rem;
			max-width: 40rem;
		}
	}
</style>
