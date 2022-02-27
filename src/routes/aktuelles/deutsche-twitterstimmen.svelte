<script>
	import TwitterEmbed from '$lib/components/TwitterEmbed.svelte';
</script>

<header>
	<div class="container">
		<a href="/" title="Aktuelles">
			<svg>
				<use xlink:href="#left-arrow" xmlns:xlink="http://www.w3.org/1999/xlink" />
			</svg>
		</a>
		<h1>Deutsche Twitterstimmen</h1>
	</div>
</header>
<main class="container">
	<div>
		<TwitterEmbed
			href="https://twitter.com/zeitonline/lists/ukraine?ref_src=twsrc%5Etfw"
			height="500"
		/>
	</div>
</main>

<style lang="scss">
	header {
		div {
			padding-top: 54px;
			padding-bottom: 24px;
			display: flex;
			align-items: center;

			h1 {
				margin-top: 0;
				font-size: 25px;
				text-align: center;
				margin-right: auto;
				margin-bottom: 0;
			}

			a {
				margin-right: auto;

				svg {
					width: 24px;
					height: 27px;
				}
			}
		}
	}
</style>
