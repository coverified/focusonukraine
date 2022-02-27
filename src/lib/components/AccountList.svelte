<script>
	import twitterAccounts from '$lib/data/twitterAccounts.json';
	import TwitterEmbed from '$lib/components/TwitterEmbed.svelte';
	let singleFeed = false;
	let twitterProfile;

	const handleImageClick = (twitterLink) => {
		singleFeed = true;
		twttr.widgets.load();
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
	{#key twitterProfile}
		<div>
			<TwitterEmbed href={twitterProfile} height="500" />
		</div>
	{/key}
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
            cursor: pointer;
			&:not(:last-of-type) {
				margin-right: 6px;
			}
		}
	}
</style>
