<script>
	import sift from '$lib/assets/sift.jpg';
	import evidence from '$lib/assets/evidence.jpg';
	import source from '$lib/assets/source.jpg';
	import context from '$lib/assets/context.jpg';
	import audience from '$lib/assets/audience.jpg';
	import purpose from '$lib/assets/purpose.jpg';
	import execution from '$lib/assets/execution.jpg';
	
	// Import Swiper Svelte components
	import FactsForFriends from '$lib/components/FactsForFriends.svelte';
	import { Swiper, SwiperSlide } from 'swiper/svelte';
	import { Pagination } from 'swiper';

	// Import Swiper styles
	import 'swiper/css';
	import 'swiper/css/pagination';
</script>

<p class="intro">
	Gezielte Propaganda erzeugt Desinformation und Verunsicherung. Wir bieten Fakten
	und Tools zum Selber-Checken.
</p>
<FactsForFriends />
<h2>Tools & Tipps</h2>
<p>
	Wir zeigen verschiedene Methoden, wie Nachrichten auf ihren Vertrauenswürdigkeit geprüft werden können, um
	Falschinformationen zuverlässig zu identifizieren.
</p>
<div class="border">
	<h2>Trust-Checking-Liste</h2>
	<p>
		Mit dieser Checkliste kannst Du in 6 einfachen Schritten direkt selbst
		überprüfen, wie vertrauenswürdig eine Information ist.
	</p>
	<a href="https://codetekt.org/" title="Codetekt" rel="noopener" target="_blank">
		Hier wirst Du Profi-Checker*in
	</a>
</div>
<Swiper
	modules={[Pagination]}
	spaceBetween={50}
	autoHeight={true}
	loop
	slidesPerView={1}
	pagination={{ clickable: true }}
>
	<SwiperSlide class="border">
		<h2>Check 1: Quelle</h2>
		<p class="fw-600">
			Die Angabe von Quellen für Behauptungen ist ein Grundbaustein für die Überprüfung der
			Glaubwürdigkeit von Informationen.
		</p>
		<ul>
			<li>
				Vergleiche den Artikel/die Nachricht mit der Originalquelle.
			</li>
			<li>
				Falls keine (Original-)Quelle angegeben ist, dann suche nach der exakten Überschrift 
				auf einer Suchmaschine deiner Wahl. Gebe die Überschrift oder Teile des Textes in 
				Anführungszeichen in die Suchmaschine ein. Beispiel “xyz”.
			</li>
			<li>	
				Der Artikel sollte keine grammatischen Fehler enthalten.
			</li>
			<li>
				Achte darauf, dass die Seite sich NICHT nur selbst zitiert und nur eigene Quellen wiedergibt.
			</li>
		</ul>
	</SwiperSlide>
	<SwiperSlide class="border">
		<h2>Check 2: Bilder & Videos</h2>
		<p class="fw-600">
			Bilder und Videos sind für uns wesentlich schneller verständlich als schriftliche
			Informationen und lösen in uns schnell negative Emotionen aus. Daher sind sie ein beliebtes
			Mittel der Manipulation der Leser*innen.
		</p>
		<ul>
			<li>	
				Falls angegeben, überprüfe die Quelle des Bildes.
			</li>
			<li>
				Die Bilder sollten einen Bezug zur der Information haben, sie dramatisieren oder skandalisieren nicht. 
			</li>
			<li>
				Nutze "Reverse Image Search", um zu sehen, ob Fotos in Artikeln oder Nachrichten authentisch sind und 
				nicht aus anderen Kontexten oder alten Informationen stammen.
			</li>
			<li>
				Für Videos: Screenshots von Videos lassen sich ebenfalls recherchieren z.B. auf:
				<a
					href="https://citizenevidence.amnestyusa.org/"
					title="Amnesty International"
					rel="noopener"
					class="text-break"
					target="_blank">https://citizenevidence.amnestyusa.org/</a
				> 
			</li>
		</ul>
	</SwiperSlide>
	<SwiperSlide class="border">
		<h2>Check 3: Inhalt</h2>
		<p class="fw-600">
			Der Text ist das Herzstück eines Artikels. Hier kann sehr kurz und reißerisch auf ein Thema
			aufmerksam gemacht oder fundiert und informativ berichtet werden. Lies genau!
		</p>
		<ul>
			<li>	
				Die Inhalte des Artikels sollten zur Überschrift passen. 
				Denn "Clickbaiting" deutet auf eine geringe Vertrauenswürdigkeit hin.
			</li>
			<li>
				Überprüfe, ob vertrauenswürdige und etablierte Medien ebenfalls über das Thema 
				berichten und zu einem ähnlichen Fazit kommen.
			</li>
			<li>
				Besuche die Webseiten von Fact-Checking Organisationen wie die von Facts for Friends, Correctiv 
				oder Mimikama und suche ob die Information dort schon aufgegriffen und überprüft wurde.?
			</li>
			<li>
				Ein professionell geschriebener Artikel ist möglichst objektiv geschrieben und frei von 
				Generalisierungen, Unterstellungen und diskriminierender Sprache. Auch wird versucht, 
				unterschiedliche Positionen im Text zum beleuchten.
			</li>
			
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
				Achte auf die "URLs". Manche Webseiten imitieren bereits bekannte Medien. 
				Beispiel: ABCnews.com vs. ABCnews.com.co.
			</li>
			<li>
				Achte auf die Qualität des Logos und Designs des Mediums. 
				Manche Webseiten versuchen die Logos bekannter Medien zu imitieren.
			</li>
			<li>
				Findet sich auf der Webseite besonders viel oder gar unseriöse Werbung, 
				deutet dies auch auf eine geringe Vertrauenswürdigkeit hin.
			</li>
		</ul>
	</SwiperSlide>
	<SwiperSlide class="border">
		<h2>Check 5: Eigentümer*innen</h2>
		<p class="fw-600">
			Achte im Impressum auf die Eigentümer*innen der Webseite und prüfe die Autor*in des Artikels.
		</p>
		<ul>
			<li>
				Achte auf die Besitzer*innen und Geldgeber*innen des Mediums mit dem betreffenden Artikel. 
				Es sollte KEINEN Verdacht auf staatliche Einflüsse (RT DE), starke politische 
				Voreingenommenheit oder Verbindungen zu Lobbygruppen geben.
			</li>
			<li>	
				Recherchiere die Personen des Artikels. Es sollte umfangreiche Informationen zu der Person geben. 
				Die Person sollte als Politikwissenschaftler*in, Journalist*in, Historiker*in und/oder Expert*in tätig sein.
			</li>
			
		</ul>
	</SwiperSlide>
	<SwiperSlide class="border">
		<h2>Check 6: Zitate</h2>
		<p class="fw-600">
			Gerade Zitate werden gerne manipuliert. Prüfe, ob das genannte Zitat verändert wurde und wer
			zitiert wird. Hat sie/er überhaupt Expertise im Feld?
		</p>
		<ul>
			<li>	
				Schau dir die Zitate im Artikel an. Überprüfe wer dieses Zitat geäußert hat. 
			</li>
			<li>
				Überprüfe, ob die in der Nachricht verwendeten Zitate mit ihrem ursprünglichen Kontext übereinstimmen. 
				In einer Suchmaschine kannst Du mit Anführungszeichen nach exakt dieser Textpassage suchen.
			</li>
			<li>
				Vergleiche die Aussagen mit öffentlich zugänglichen Studien und anerkannten Expert*innen im jeweiligen Gebiet.
			</li>
			
		</ul>
	</SwiperSlide>
</Swiper>
<div class="border mt-3 pb-0">
	<h2>SIFT-Methode</h2>
	<p>
		Mike Caulfield, Director of Blended and Networked Learning der Washington State University,
		empfiehlt die 4 Schritte: stoppen, recherchieren, finden, nachverfolgen.
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
		Zielgruppe, Zweck und Darstellung.
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
