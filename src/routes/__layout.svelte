<script>
	import Icons from '$lib/components/Icons.svelte';
	import Nav from '$lib/components/Nav.svelte';
	import Footer from '$lib/components/Footer.svelte';
</script>

<Icons />

<header class="d-sm-none">
	<Nav />
</header>

<main class="container d-sm-none">
	<slot />
</main>

<main class="d-none d-sm-block landingpage">
	<div class="container">
		<h1>
			FocusOn
			<span class="sr-only">Ukraine</span>
			<svg class="">
				<use xlink:href="#ukraine" xmlns:xlink="http://www.w3.org/1999/xlink" />
			</svg>
			<span class="d-block small">Einfach vielfältig informiert</span>
		</h1>
		<h2>Mobile First!</h2>
		<p>
			#FocusOnUkraine bündelt vielfältige, vertrauenswürdige Informationen zum Krieg in der Ukraine.<br
			/>
			Diese Plattform ist sehr kurzfristig entstanden und konzentriert sich erstmal auf die mobile Darstellung.<br
			/>
			Desktop Ansicht ist in Arbeit. Wenn du Entwickler:in bist und uns dabei unterstützen möchtest,
			melde dich gerne!
		</p>
		<h3>
			Ruf die Seite auf deinem Handy auf oder zieh deinen Browser kleiner bis auf Handygröße, dann
			kannst du alle Inhalte sehen
		</h3>
		<div class="en">
			<p>
				#FocusOnUkraine is a pool for a wide range of reliable informations about the war in Ukraine.
				This platform came to life in a very short period of time and starts with a focus on mobile
				view. Desktop view coming soon. If you happen to be a developer and want to support us, please
				get in touch!
			</p>
			<h3>
				Open this page on your mobile device or scale your browser down to mobile size to see all the
				content.
			</h3>
		</div>
	</div>
</main>

<Footer />

<style type="text/scss">
	@font-face {
		font-family: 'Barlow';
		font-style: normal;
		font-weight: 300;
		font-display: swap;
		src: url('/fonts/Barlow/Barlow-Light.ttf') format('truetype');
	}

	@font-face {
		font-family: 'Barlow';
		font-style: normal;
		font-weight: 400;
		font-display: swap;
		src: url('/fonts/Barlow/Barlow-Regular.ttf') format('truetype');
	}

	@font-face {
		font-family: 'Barlow';
		font-style: normal;
		font-weight: 500;
		font-display: swap;
		src: url('/fonts/Barlow/Barlow-Medium.ttf') format('truetype');
	}
	@font-face {
		font-family: 'Barlow';
		font-style: normal;
		font-weight: 600;
		font-display: swap;
		src: url('/fonts/Barlow/Barlow-SemiBold.ttf') format('truetype');
	}
	@font-face {
		font-family: 'Barlow';
		font-style: italic;
		font-weight: 600;
		font-display: swap;
		src: url('/fonts/Barlow/Barlow-SemiBoldItalic.ttf') format('truetype');
	}
	@font-face {
		font-family: 'Barlow';
		font-style: normal;
		font-weight: 700;
		font-display: swap;
		src: url('/fonts/Barlow/Barlow-Bold.ttf') format('truetype');
	}
	@font-face {
		font-family: 'Barlow Condensed';
		font-style: normal;
		font-weight: 600;
		font-display: swap;
		src: url('/fonts/BarlowCondensed/BarlowCondensed-SemiBold.ttf') format('truetype');
	}
	:global(:root) {
		--color-primary: #005bbb;
		--color-secondary: #fed500;
		--color-black: #000;
		--color-white: #fff;
		--body-color: #383840;
		--bs-gutter-x: 1.6875rem;

		overflow-x: hidden;
	}

	:global(body) {
		font-size: 1rem;
		color: var(--body-color);
		font-family: 'Barlow', sans-serif;
		height: 100%;
	}

	:global(main) {
		position: relative;
		min-height: calc(100vh - 289px);
		overflow: hidden;
	}

	:global(h1, h2, h3, h4) {
		font-family: 'Barlow Condensed';
	}

	:global(h1) {
		font-size: 2.1875rem;
	}

	:global(h2) {
		font-size: 1.25rem;
		margin-top: 2rem;
		margin-bottom: 0.5rem;
	}

	:global(header) {
		background-color: var(--color-secondary);
		width: 100%;
	}

	:global(a) {
		color: var(--color-primary);
	}

	:global(.intro) {
		font-weight: 600;
		font-size: 0.875rem;
		font-style: italic;
		margin-top: 2.3125rem;
		padding: 0 1.6875rem;
	}

	:global(.swiper-slide) {
		background-color: var(--color-secondary);
		padding: 14px 12px 21px 12px;

		:global(ul) {
			margin-bottom: 23px;
		}

		:global(h2) {
			margin-top: 0;
			margin-bottom: 0.75rem;
		}
	}

	.landingpage {
		background-color: var(--color-secondary);
		width: 100%;
		height: 100vh;
		text-align: center;
		
		p {
			font-weight: 600;
			font-style: italic;
			margin-bottom: 3rem;
		}

		h1 {
			padding-top: 1.375rem;
			text-align: center;
			color: var(--color-primary);
			margin-bottom: 2.1875rem;

			svg {
				width: 145px;
				height: 51px;
				margin-top: -12px;
			}

			span {
				font-size: 1rem;
			}
		}

		h2 {
			font-size: 3rem;
			font-weight: 600;
			font-style: italic;
			margin-top: 8rem;
			margin-bottom: 4rem;
		}

		.en {
			margin-top: 5rem;
			color: var(--color-primary);
		}
	}

	@media (max-width: 768px) {
		:global(::-webkit-scrollbar) {
			display: none;
		}
	}
</style>
