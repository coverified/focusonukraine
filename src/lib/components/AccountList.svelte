<script>
	import twitterAccounts from '$lib/data/twitterAccounts.json';
	import TwitterEmbed from '$lib/components/TwitterEmbed.svelte';
	let singleFeed = false;
	let activeItem;
	let twitterProfile;

	const handleImageClick = (twitterLink, index) => {
		twttr.widgets.load();
		singleFeed = true;
		activeItem = index;
		twitterProfile = twitterLink;
	};
</script>

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

	.twitter__wrapper {
		margin-top: 7.1875rem;
	}

	ul {
		display: flex;
		list-style-type: none;
		padding-left: 0;
		width: 100%;
		overflow: auto;
		white-space: nowrap;
		position: absolute;
		left: 0;
		padding-left: 27px;
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
		}
	}
</style>
