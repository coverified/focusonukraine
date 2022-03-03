<script>
	const endpoint = 'https://fff-ingest.s3.eu-central-1.amazonaws.com/katapult_ukraine.json';

	const getData = async () => {
		const response = await fetch(endpoint);
		const result = await response.json();
		return result;
	};

	let promise = getData();
</script>

<h2>Katapultmagazin</h2>
<p>
	KATAPULT baut aus Statistiken und Studien der Sozialwissenschaften vereinfachte und detaillierte
	Grafiken. Die Artikel werden von Wissenschaftlern und Redakteuren verfasst.
</p>
<div class="height">
	{#await promise then data}
		{#each data as item}
			<img src={item.images} alt={item.content} />
			<p>{item.content}</p>		
			<hr />
		{/each}
	{/await}
</div>

<style lang="scss">
	.height {
		max-height: 25rem;
		overflow: auto;
		padding: 0 12px 21px 12px;
		border: 1px solid var(--border-color);

		img {
			width: calc(100% + 24px);
			height: 174px;
			object-fit: cover;
			margin-bottom: 1rem;
			margin-right: -12px;
			margin-left: -12px;
		}


		h2 {
			&:first-of-type {
				margin-top: 0.5rem;
			}
		}
	}

	@media (min-width: 768px) {
		.height {
			max-height: 40rem;
			max-width: 40rem;
		}
	}
</style>
