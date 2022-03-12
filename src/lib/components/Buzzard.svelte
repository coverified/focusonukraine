<script>
	import Buzzard from '$lib/assets/buzzard.png';

	const endpoint = '/api/buzzard';

	const getData = async () => {
		const response = await fetch(endpoint);
		return await response.json();
	};

	let promise = getData();
</script>

<h2>The Buzzard</h2>
<p>
	„Buzzard“ ist eine neue News-App für Perspektiven-Vielfalt, die zu den Top-Themen des Tages
	Medienbeiträge des ganzen politischen Spektrums bündelt und journalistisch einordnet.
</p>
<div class="height">
	{#await promise then data}
		{#each data as item}
			<h2>{item.title}</h2>
			<a href={item.url} rel="noopener" target="_blank" title={item.linktext} class="fact-link">
				{item.linktext}
			</a>
		{/each}
	{/await}
</div>
<a
	href="https://www.buzzard.org/"
	title="https://www.buzzard.org/"
	rel="noopener"
	class="link"
	target="_blank"
>
	<img src={Buzzard} alt="https://www.buzzard.org/" /> www.buzzard.org
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
