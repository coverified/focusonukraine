<script>
	import piqd from '$lib/assets/piqd.png';

	const endpoint = 'https://fff-ingest.s3.eu-central-1.amazonaws.com/piqd.json';

	const getData = async () => {
		const response = await fetch(endpoint);
		const result = await response.json();
		return result;
	};

	let promise = getData();
</script>

<h2>piqd</h2>
<p>
	Rund 100 kluge Köpfe empfehlen hier täglich ausgewählte “piqs” – Artikel, Reportagen, Interviews
	und mehr mit geprüft guten Inhalten aus tausenden von Quellen.
</p>
<div class="height">
	{#await promise then data}
		{#each data as item}
			<h2>{item.headline}</h2>
			<a href={item.url} rel="noopener" target="_blank" title="Mehr erfahren" class="fact-link">
				Mehr erfahren
			</a>
		{/each}
	{/await}
</div>
<a href="https://www.piqd.de/" title="piqd.de" rel="noopener" class="link" target="_blank">
	<img src={piqd} alt="Piqd" />piqd.de
</a>

<style lang="scss">
	.height {
		max-height: 25rem;
		overflow: auto;
		padding: 0 12px 21px 12px;
		border: 1px solid var(--border-color);

		h2 {
			&:first-of-type {
				margin-top: 0.5rem;
			}
		}
	}

	.link {
		font-size: 1.25rem;
		display: block;
		margin-top: 1rem;
		text-decoration: none;

		img {
			margin-right: 0.5rem;
		}
	}

	@media (min-width: 768px) {
		.height {
			max-height: 40rem;
			max-width: 40rem;
		}
	}
</style>
