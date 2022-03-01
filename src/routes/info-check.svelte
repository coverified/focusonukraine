<script>
	import sift from '$lib/assets/sift.jpg';
	import evidence from '$lib/assets/evidence.jpg';
	import source from '$lib/assets/source.jpg';
	import context from '$lib/assets/context.jpg';
	import audience from '$lib/assets/audience.jpg';
	import purpose from '$lib/assets/purpose.jpg';
	import execution from '$lib/assets/execution.jpg';

	// Import Swiper Svelte components
	import { Swiper, SwiperSlide } from 'swiper/svelte';
	import { Pagination } from 'swiper';

	// Import Swiper styles
	import 'swiper/css';
	import 'swiper/css/pagination';
</script>

<p class="intro">
	Gezielte Propaganda erzeugt Desinformation und Verunsicherung. Wir bieten Euch Fakten statt Fake
	und Tools zum Selber-Checken.
</p>
<!-- TODO Factsforfriends.de Einbindung -->
<h2>Tools & Tipps</h2>
<p>
	Verschiedene Methoden, wie Ihr Nachrichten auf ihren Wahrheitsgehalt prüfen könnt, um
	Falschinformationen zuverlässig zu identifizieren.
</p>
<div class="border">
	<h2>Fact-Check-Liste</h2>
	<p>
		Fake oder Fakt? Mit dieser Checkliste kannst du das in 6 einfachen Schritten direkt selbst
		überprüfen.
	</p>
	<a href="https://codetekt.org/" title="Codetekt" rel="noopener" target="_blank">
		Hier wirst du Profi-Checker*in
	</a>
</div>
<Swiper
	modules={[Pagination]}
	spaceBetween={50}
	autoHeight={true}
	loop
	slidesPerView={1}
	pagination={{ clickable: true }}
	on:slideChange={() => console.log('slide change')}
	on:swiper={(e) => console.log(e.detail[0])}
>
	<SwiperSlide class="border">
		<h2>Check 1: Quelle</h2>
		<p class="fw-600">
			Die Angabe von Quellen für Behauptungen ist ein Grundbaustein für die Überprüfung der
			Glaubwürdigkeit von Informationen.
		</p>
		<ul>
			<li>
				Wird im Text die Originalquelle genannt? Vergleiche den Artikel/die Nachricht mit dieser
				Originalquelle.
			</li>
			<li>
				Suche nach der exakten Überschrift auf einer Suchmaschine deiner Wahl. Hilfreich sind dabei
				Suchoperatoren wie “Text”.
			</li>
			<li>Weist der Artikel grammatikalische Fehler auf?</li>
			<li>
				Achte darauf, dass die Seite sich nicht nur selbst zitiert und eigene Quellen wiedergibt.
			</li>
		</ul>
	</SwiperSlide>
	<SwiperSlide class="border">
		<h2>Check 2: Bilder & Videos</h2>
		<p class="fw-600">
			Bilder und Videos sind für uns wesentlich schneller verständlich als schriftliche
			Informationen und lösen in uns schnell negative Emotionen aus. Daher sind Sie ein beliebtes
			Mittel der Manipulation der Leser:innen.
		</p>
		<ul>
			<li>Falls angegeben, die Quelle des Bildes prüfen.</li>
			<li>
				Die Bilder sollten einen Bezug zur Aussage haben, sie dramatisieren oder skandalisieren
				nicht.
			</li>
			<li>
				Nutze Reverse Image Search, um zu sehen, ob Fotos in Artikeln oder Nachrichten authentisch
				sind und nicht aus anderen Kontexten stammen. Ein Tool dafür ist Tineye oder GOOGLE IMAGE
				SEARCH per Drag+Drop
			</li>
			<li>
				Für Videos: Screenshots lassen sich ebenfalls mit Reverse Image Search recherchieren.
				<a
					href="https://citizenevidence.amnestyusa.org/"
					title="Amnesty International"
					rel="noopener"
					target="_blank">https://citizenevidence.amnestyusa.org/</a
				> (Bietet dies direkt an)
			</li>
		</ul>
	</SwiperSlide>
	<SwiperSlide class="border">
		<h2>Check 3: Inhalt</h2>
		<p class="fw-600">
			Der Text ist das Herzstück eines Artikels. Hier kann sehr kurz und reißerisch auf ein Thema
			aufmerksam gemacht werden oder fundiert und informativ berichtet werden. Lies genau!
		</p>
		<ul>
			<li>Passen die Inhalte des Artikels zur Überschrift?</li>
			<li>
				Berichten verlässliche Medien ebenfalls über das Thema und kommen zu einem ähnlichen Fazit?
			</li>
			<li>
				Enthält der Artikel Behauptungen, die bei professionellen Medienhäusern -
				öffentlich-rechtliche Medien, etablierte Wochenzeitungen oder Fachmedien - nicht vorkommen?
			</li>
			<li>
				Wurde der Inhalt bereits von Fact-Checking Organisationen wie Correktiv, Faktenfinder, Facts
				for Friends oder Mimikama aufgegriffen und geprüft?
			</li>
			<li>
				Ist der Artikel ist möglichst objektiv geschrieben und frei von Generalisierungen,
				Unterstellungen und diskriminierender Sprache?
			</li>
			<li>Werden beide Seiten einer Debatte/ unterschiedliche Positionen dargestellt?</li>
		</ul>
	</SwiperSlide>
	<SwiperSlide class="border">
		<h2>Check 4: Online-Präsenz</h2>
		<p class="fw-600">
			Ein Blick auf die Homepage verrät bereits viel über die Vertrauenswürdigkeit. Achte auf URL
			und Werbung.
		</p>
		<ul>
			<li>
				Achte auf die URLs. Manche Webseiten imitieren bereits bekannte Medien. Beispiel:
				ABCnews.com vs. ABCnews.com.co.
			</li>
			<li>
				Achte auf die Qualität des Logos und Designs des Mediums: Versucht die Webseite das Logo
				bekannter Medien zu imitieren?
			</li>
			<li>
				Findet sich auf der Webseite besonders viel oder gar unseriöse Werbung deutet dies auch auf
				eine geringe Vertrauenswürdigkeit hin.
			</li>
		</ul>
	</SwiperSlide>
	<SwiperSlide class="border">
		<h2>Check 5: Eigentümer*innen</h2>
		<p class="fw-600">
			Achte im Impressum auf die Eigentümer der Webseite und prüfe den Autor des Artikels.
		</p>
		<ul>
			<li>
				Achte auf die Besitzer*innen und Geldgeber*innen des Mediums mit dem betreffenden Artikel.
				Gibt es einen Verdacht auf staatliche Einflüsse (RT DE), starken politischen Bias (Junge
				Freiheit oder Linksunten-indymedia) oder Verbindungen zu Lobbygruppen?
			</li>
			<li>Recherchiere die Personen des Artikels/Textes:</li>
			<li>Ist es ein*e bekannte*r Journalist*in, Autor*in?</li>
		</ul>
	</SwiperSlide>
	<SwiperSlide class="border">
		<h2>Check 6: Zitate</h2>
		<p class="fw-600">
			Gerade Zitate werden gerne manipuliert. Prüfe, ob das genannte Zitat verändert wurde und wer
			zitiert wird. Hat er überhaupt Expertise im Feld?
		</p>
		<ul>
			<li>Schau dir die Zitate im Artikel/Text an. Wer hat diese geäußert?</li>
			<li>Handelt es sich um Expert*innen auf dem speziellen Gebiet?</li>
			<li>
				Stimmen die in der Nachricht verwendeten Zitate mit ihrem ursprünglichen Kontext überein?
				-In einer Suchmaschine kannst Du mit Anführungszeichen nach exakt dieser Textpassage suchen.
			</li>
			<li>
				Vergleiche die Aussagen mit öffentlich zugänglichen Studien und anerkannten Expert*innen im
				jeweiligen Gebiet.
			</li>
			<li>
				Kommen in der Nachricht identifizierbare Personen (beispielsweise mit vollständigem Namen
				und/oder Wohnort) direkt oder indirekt zu Wort?
			</li>
		</ul>
	</SwiperSlide>
</Swiper>
<div class="border mt-3 pb-0">
	<h2>SIFT-Methode</h2>
	<p>
		Mike Caulfield, Director of Blended and Networked Learning der Washington State University
		empfiehlt die 4 Schritte: Stoppen, recherchieren, finden, nachverfolgen.
	</p>
	<a
		href="https://researchguides.uoregon.edu/c.php?g=612324&p=7297194"
		title="Mehr zu SIFT"
		rel="noopener"
		target="_blank"
		class="mb-4"
	>
		Mehr zu SIFT
	</a>
	<img src={sift} alt="SIFT" width="335px" height="613px" />
</div>
<div class="border mt-3 pb-0 mb-5">
	<h2>ESCAPE-Methode</h2>
	<p>
		Vom Bildungsanbieter für Medienkompetenz, NewseumED.org, stammt diese Methode, die Informationen
		anhand von 6 aufeinanderfolgenden Evaluationsphasen beurteilt: Beweis, Quelle, Kontext,
		Zielgruppem Zweck und Darstellung.
	</p>
	<a
		href="https://lakeland.libguides.com/c.php?g=696342&p=5309560"
		title="Mehr zu ESCAPE"
		rel="noopener"
		class="mb-4"
		target="_blank"
	>
		Mehr zu ESCAPE
	</a>
	<img src={evidence} alt="evidence" width="335px" height="702px" />
	<img src={source} alt="source" width="335px" height="702px" />
	<img src={context} alt="context" width="335px" height="702px" />
	<img src={audience} alt="audience" width="335px" height="702px" />
	<img src={purpose} alt="purpose" width="335px" height="702px" />
	<img src={execution} alt="execution" width="335px" height="702px" />
</div>

<style lang="scss">
	.fw-600 {
		font-weight: 600;
	}

	.border {
		padding: 20px 12px 21px 12px;

		a {
			display: block;
		}

		img {
			margin-right: -12px;
			margin-left: -12px;
		}

		h2 {
			margin-top: 0;
		}
	}
</style>
