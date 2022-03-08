<script>
	import LinkedInLogo from '$lib/assets/linkedin-logo.png';
	import TwitterLogo from '$lib/assets/twitter-logo.png';
</script>

<footer>
	<div class="container">
		<div class="row align-items-center py-0 text-center justify-content-center">
			<div class="col-6 col-md-3">
				<a
					href="https://www.linkedin.com/company/digital-democracy-alliance/?originalSubdomain=de"
					title="LinkeIn"
					target="_blank"
					rel="noopener"
				>
					<img src={LinkedInLogo} alt="LinkedIn" width="50px" class="d-flex mx-auto" />
				</a>
			</div>
			<div class="col-6 col-md-3">
				<a href="https://twitter.com/DDAlliance_org" title="Twitter" target="_blank" rel="noopener">
					<img src={TwitterLogo} alt="LinkedIn" width="50px" class="d-flex mx-auto" />
				</a>
			</div>
			<div class="col-6 col-md-3">
				<a href="/impressum" title="Impressum"> Impressum </a>
			</div>
			<div class="col-6 col-md-3">
				<a href="/datenschutzerklaerung" title="Datenschutzerklaerung"> Datenschutzerklärung </a>
			</div>
		</div>
	</div>
</footer>

<style lang="scss">
	footer {
		background-color: var(--color-secondary);
		width: 100%;
		margin-top: 2rem;
	}

	img {
		width: 50px;
		height: auto;
	}

	div {
		padding-top: 1rem;
		padding-bottom: 1rem;

		a {
			text-decoration: none;

			&:not(:last-of-type) {
				margin-right: 1rem;
			}
		}
	}
</style>
