<script>
	import Buzzard from '$lib/assets/buzzard.png';
</script>

<h2><span>coming soon:</span> The Buzzard</h2>
<p>
	„Buzzard“ ist eine neue News-App für Perspektiven-Vielfalt, die zu den Top-Themen des Tages
	Medienbeiträge des ganzen politischen Spektrums bündelt und journalistisch einordnet.
</p>

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
		height: 35rem;
		overflow: auto;
		padding: 0 12px 21px 12px;
		border: 1px solid var(--border-color);

		img {
			width: calc(100% + 24px);
			height: 21.25rem;
			object-fit: contain;
			margin-bottom: 1rem;
			margin-right: -12px;
			margin-left: -12px;
		}

		h2 {
			span {
				font-weight: 300;
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
