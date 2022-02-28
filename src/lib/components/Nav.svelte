<script>
	import { page } from '$app/stores';
</script>

<div class="container">
	<h1>
		FocusOn
		<svg class="">
			<use xlink:href="#ukraine" xmlns:xlink="http://www.w3.org/1999/xlink" />
		</svg>
		<span class="d-block small">Einfach vielfältig informiert</span>
	</h1>
	<nav>
		<a title="Aktuelles" href="." sveltekit:prefetch class:active={$page.url.pathname === '/'}>
			<svg class="">
				<use xlink:href="#magnifying-glass" xmlns:xlink="http://www.w3.org/1999/xlink" />
			</svg>
			Aktuelles
		</a>
		<a
			title="Hintergründe"
			href="/hintergruende"
			sveltekit:prefetch
			class:active={$page.url.pathname === '/hintergruende'}
		>
			<svg class="">
				<use xlink:href="#magnifying-glass" xmlns:xlink="http://www.w3.org/1999/xlink" />
			</svg>
			Hintergründe
		</a>
		<a
			title="InfoCheck"
			href="info-check"
			sveltekit:prefetch
			class:active={$page.url.pathname === '/info-check'}
		>
			<svg class="">
				<use xlink:href="#magnifying-glass" xmlns:xlink="http://www.w3.org/1999/xlink" />
			</svg>
			InfoCheck
		</a>
		<a
			title="Kriterien"
			href="kriterien"
			sveltekit:prefetch
			class:active={$page.url.pathname === '/kriterien'}
		>
			<svg class="">
				<use xlink:href="#magnifying-glass" xmlns:xlink="http://www.w3.org/1999/xlink" />
			</svg>
			Kriterien
		</a>
		<a
			title="Was wir machen"
			href="ueber-uns"
			sveltekit:prefetch
			class:active={$page.url.pathname === '/ueber-uns'}
		>
			<svg class="">
				<use xlink:href="#magnifying-glass" xmlns:xlink="http://www.w3.org/1999/xlink" />
			</svg>
			Was wir machen
		</a>
	</nav>
</div>

<style lang="scss">
	div {
		h1 {
			padding-top: 3.375rem;
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

		nav {
			width: 100%;
			overflow: auto;
			white-space: nowrap;
			padding-bottom: 1.125rem;

			svg {
				width: 20px;
				height: 13px;
			}

			a {
				text-decoration: none;
				font-weight: 600;

				&:not(:last-of-type) {
					margin-right: 2.375rem;
				}
			}

			.active {
				box-shadow: inset 0 -3px 0 0 var(--color-primary);
				padding-bottom: 1.3125rem;
			}
		}
	}

	::-webkit-scrollbar {
		display: none;
	}
</style>
