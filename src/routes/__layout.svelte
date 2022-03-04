<script>
	import Icons from '$lib/components/Icons.svelte';
	import Nav from '$lib/components/Nav.svelte';
	import Footer from '$lib/components/Footer.svelte';
</script>

<Icons />

<header>
	<Nav />
</header>

<main class="container">
	<slot />
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
		--border-color: #dee2e6;
		--bs-gutter-x: 1.6875rem;

		overflow-x: hidden;
	}

	@media (min-width: 1400px) {
		:global(.container)  {
			max-width: 960px;
		}
	}

	@media (min-width: 1200px) {
		:global(.container) {
			max-width: 960px;
		}
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

	:global(.sr-only) {
		display: none;
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

	@media (max-width: 768px) {
		:global(::-webkit-scrollbar) {
			display: none;
		}
	}
</style>
