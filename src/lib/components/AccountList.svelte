<script>
	import TwitterEmbed from '$lib/components/TwitterEmbed.svelte';

	let singleFeed = false;
	let activeItem;
	let twitterProfile;

	export let twitterAccounts;

	const handleImageClick = (twitterLink, index) => {
		twttr.widgets.load();
		activeItem = index;
		twitterProfile = twitterLink;
		singleFeed = true;
	};
</script>

<div class="account-list">
	<h2>Einzelne Accounts auswählen</h2>
	<ul>
		{#each twitterAccounts as { twitterName, twitterLink, image }, index}
			<li
				on:click={() => {
					handleImageClick(twitterLink, index);
				}}
			>
				<img
					src={image}
					loading="lazy"
					alt={twitterName}
					width="70"
					height="70"
					class={activeItem === index ? 'active' : ''}
				/>
				<p>
					{twitterName}
				</p>
			</li>
		{/each}
	</ul>
	{#if singleFeed}
		{#key twitterProfile}
			<div class="twitter__wrapper">
				<TwitterEmbed href={twitterProfile} height="500" />
			</div>
		{/key}
	{/if}
</div>

<style lang="scss">
	img {
		width: 70px;
		height: 70px;
		display: block;
		border-radius: 5rem;
	}

	.active {
		border: 3px solid var(--color-primary);
	}

	h2 {
		margin-top: 2.8125rem;
	}

	ul {
		display: flex;
		list-style-type: none;
		padding-left: 0;
		width: 100vw;
		overflow: auto;
		white-space: nowrap;
		padding-top: 0.5rem;

		li {
			cursor: pointer;
			display: flex;
			flex-direction: column;
			align-items: center;
			color: var(--body-color);
			font-size: 0.6875rem;
			margin-right: 8px;

			p {
				margin-top: 0.5rem;
			}

			&:last-of-type {
				padding-right: 2.5rem;
			}
		}
	}

	@media (min-width: 576px) {
		ul {
			width: 100%;

			li {
				&:last-of-type {
					padding-right: 0;
				}
			}
		}
	}
</style>
