<script>
	import logo from '$lib/assets/logo.svg';
	import Codeetekt from '$lib/assets/codetekt_rgb.svg';
	import Coverified from '$lib/assets/coverified.svg';
	import Factsforfriends from '$lib/assets/factsforfriends.svg';
	import Piqd from '$lib/assets/piqd_blue.svg';
	import Buzzard from '$lib/assets/buzzard-logo.png';
</script>

<p class="intro">
	Krisensituationen bedürfen Krisenkommunikation. Für uns bedeutet das nicht nur Bündelung
	verlässlicher Informationen sondern vor allem Bündelung starker Kompetenzen.
</p>
<h2>Unser Antrieb</h2>
<p>
	Falschinformationen in sozialen Netzwerken, gezielte Desinformation und Propaganda – der Angriff
	auf die Ukraine spielt sich auch im Netz ab. #FocusOnUkraine bündelt die Vielzahl an Inhalten aus
	geprüften Quellen an einem Ort und hilft, in dieser Informationsflut den Überblick zu behalten.
</p>
<p>
	Aktuelle Tweets nach strengen Kriterien ausgewählter Twitter-Kanäle, Hintergrundwissen seriöser
	Medien und Faktenchecks bieten die Möglichkeit, sich mit Hilfe dieser Plattform umfassend zur Lage
	in der Ukraine zu informieren - ohne langwierigen Rechercheaufwand.
</p>
<h2>Unser Team</h2>
<p>
	#FocusOnUkraine ist ein Projekt der <a
		href="https://digital-democracy-alliance.org/"
		title="Digital Democracy Alliance"
		rel="noopener"
		target="_blank">Digital Democracy Alliance</a
	> – ein Zusammenschluss verschiedener Initiativen mit dem Ziel, digitale Lösungen gegen Desinformation
	zu schaffen, Medienkompetenz aufzubauen und durch informierte Kommunikation Demokratie zu stärken –
	auch über Landesgrenzen hinaus.
</p>

<h2>We #StandWithUkraine</h2>
<img src={logo} alt="Digital Democracy Alliance" class="mb-4" />
<h2>Die beteiligten Initiativen der DDA</h2>
<div class="row align-items-center mt-4 logos">
	<div class="col-sm-4">
		<img src={Coverified} alt="Coverified" class="mb-4" />
	</div>
	<div class="col-sm-4">
		<img src={Codeetekt} alt="Codeetekt" class="mb-4" />
	</div>
	<div class="col-sm-4">
		<img src={Factsforfriends} alt="Factsforfriends" class="mb-4" />
	</div>
</div>
<h2>Inhaltliche Kooperation mit</h2>
<div class="row logos mt-4">
	<div class="col-sm-4">
		<img src={Piqd} alt="Piqd" class="mb-4" />
	</div>
	<div class="col-sm-4">
		<img src={Buzzard} alt="Buzzard" class="mb-4 buzzard" />
	</div>
</div>

<!-- <TODO Logos Katapult qiqd, the buzzard einfügen> -->
<style lang="scss">
	.buzzard {
		width: 300px;
		margin-left: 2rem;
	}

	@media (max-width: 576px) {
		.logos {
			img {
				width: 150px;
			}
		}
	}
</style>
