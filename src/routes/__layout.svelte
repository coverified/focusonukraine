<script>
	import Icons from '$lib/components/Icons.svelte';
	import Nav from '$lib/components/Nav.svelte';
</script>

<Icons />

<header>
	<Nav />
</header>

<main class="container">
	<slot />
</main>

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
	}

	main {
		position: relative;
	}

	:global(h1, h2, h3, h4) {
		font-family: 'Barlow Condensed';
	}

	:global(h1) {
		font-size: 2.1875rem;
	}

	:global(h2) {
		font-size: 1.25rem;
		margin-top: 2.0625rem;
		margin-bottom: 0.5rem;
	}

	:global(::-webkit-scrollbar) {
		display: none;
	}

  :global(header) {
    background-color: var(--color-secondary);
		width: 100%;
  }
</style>
