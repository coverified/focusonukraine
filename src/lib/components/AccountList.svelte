<script>
	import twitterAccounts from '$lib/data/twitterAccounts.json';
	import TwitterEmbed from './TwitterEmbed.svelte';

	let singleFeed = false;
	let twitterProfile;

	const handleImageClick = (twitterLink) => {    
		singleFeed = true;
		twitterProfile = twitterLink;
	};
</script>

<ul>
	{#each twitterAccounts as { twitterName, twitterLink, image }, index}
		<li
			on:click={() => {
				handleImageClick(twitterLink);
			}}
		>
			<image src={image} alt={twitterName} width="70" height="70" />
			<p>
				{twitterName}
			</p>
		</li>
	{/each}
</ul>
{#if singleFeed}
	<TwitterEmbed href={twitterProfile} height="500" />
{/if}

<style lang="scss">
	image {
		width: 70px;
		height: 70px;
		display: block;
	}

	ul {
		display: flex;
		list-style-type: none;

		li {
			&:not(:last-of-type) {
				margin-right: 6px;
			}
		}
	}
</style>
