<script>
	import Icons from '$lib/components/Icons.svelte';
	import Nav from '$lib/components/Nav.svelte';
	import Footer from '$lib/components/Footer.svelte';
	import Mockup from '$lib/assets/landingpage_image.png';

	let desktopView;

	const handleClick = () => {
		desktopView = true;
	};
</script>

<Icons />

<header class={desktopView ? '' : 'd-sm-none'}>
	<Nav/>
</header>

<main class="container {desktopView ? '' : 'd-sm-none'}">
	<slot />
</main>

<main class="d-none {desktopView ? 'd-none' : 'd-sm-block'} landingpage">
	<div class="container">
		<h1>
			FocusOn
			<span class="sr-only">Ukraine</span>
			<svg>
				<use xlink:href="#ukraine" xmlns:xlink="http://www.w3.org/1999/xlink" />
			</svg>
			<span class="d-block small">Einfach vielfältig informiert</span>
		</h1>
		<div class="row align-items-center">
			<div class="col-lg-8">
				<h2>Desktopversion in Arbeit...</h2>
				<p>
					Diese Webseite ist für Mobilgeräte optimiert:<br />
					Verkleinere Dein Browserfenster seitlich oder öffne die Seite auf Deinem Handy.
				</p>
				<button
					on:click={() => {
						handleClick();
					}}
				>
					Trotzdem zur Desktop-Ansicht wechseln?<br /> Bitte beachte: Diese ist noch in Bearbeitung.
					Daher entsprechen zwar die Inhalte, nicht aber die Darstellung der fertigen Version.
				</button>
			</div>
			<div class="col-lg-4">
				<img src={Mockup} alt="Mobile View Mockup" width="442" />
			</div>
		</div>
	</div>
</main>

<div class={desktopView ? '' : 'd-sm-none'}>
	<Footer />
</div>

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

	.landingpage {
		background-color: var(--color-secondary);
		width: 100%;
		height: 100vh;

		p {
			font-size: 2rem;
			font-weight: 600;
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
			margin-top: 0;
			margin-bottom: 4rem;
		}

		.text-primary {
			color: var(--color-primary) !important;
		}

		button {
			padding: 15px;
			padding-left: 4.5rem;
			color: var(--color-primary);
			font-size: 18px;
			width: 440px;
			border-radius: 15px;
			appearance: none;
			background-color: var(--color-white);
			text-align: left;
			position: relative;

			&:before {
				content: '\2192';
				position: absolute;
				left: 13px;
				font-size: 40px;
				top: 25%;
			}
		}

		.row {
			margin-top: 10rem;
		}
	}

	@media (max-width: 768px) {
		:global(::-webkit-scrollbar) {
			display: none;
		}
	}
</style>
