<script>
	// Import Swiper Svelte components
	import { Swiper, SwiperSlide } from 'swiper/svelte';
	import { Pagination } from 'swiper';

	// Import Swiper styles
	import 'swiper/css';
	import 'swiper/css/pagination';
</script>

<p class="intro">
	Um seriöse Informationen bereitzustellen wurden für die Auswahl der auf #FocusOnUkraine 
	hinterlegten Quellen eigens strenge Kriterienkataloge erstellt.
</p>
<h2>Unsere Kriterien für Twitter</h2>
<p>
	Für die Kategorie “Aktuelles” haben wir Twitter-Listen mit diversen Stimmen zur Ukraine-Krise
	erstellt. Die einzelnen Accounts auf den Twitter-Listen erfüllen mindestens eine oder mehrere der
	folgenden Kriterien:
</p>
<Swiper
	modules={[Pagination]}
	spaceBetween={50}
	autoHeight={true}
	loop
	slidesPerView={1}
	pagination={{ clickable: true }}
    class="mb-5 swiper-slideshow-primary"
>
	<SwiperSlide class="border swiper-slide-primary">
		<h2>1. Transparenz</h2>
		<p>
			Es gibt umfangreiche Informationen zu der Person - wie Herkunft, Ausbildung, Studium,
			Berufserfahrung und Beschäftigung.
		</p>
	</SwiperSlide>
	<SwiperSlide class="border swiper-slide-primary">
		<h2>2. Erfahrung</h2>
		<p>
			Die Person hat mehrjährige Erfahrung als Politikwissenschaftler*in, Journalist*in,
			Historiker*in, Expert*in
		</p>
	</SwiperSlide>
	<SwiperSlide class="border swiper-slide-primary">
		<h2>3. Medienzitate</h2>
		<p>Die Person wurde mehrfach von verschiedenen Medien zu dem Thema befragt und/oder zitiert</p>
	</SwiperSlide>
	<SwiperSlide class="border swiper-slide-primary">
		<h2>4. Empfehlungen</h2>
		<p>
			Die Person wurde mehrfach von verschiedenen Medien und/oder Expert*innen zu diesem Thema
			empfohlen.
		</p>
	</SwiperSlide>
	<SwiperSlide class="border swiper-slide-primary">
		<h2>5. Themenfokus</h2>
		<p>
			Der Hauptfokus des Accounts liegt auf dem Krieg in der Ukraine und bietet aktuelle 
			sowie zurückliegende Informationen.
		</p>
	</SwiperSlide>
	<SwiperSlide class="border swiper-slide-primary">
		<h2>6. Medien vor Ort</h2>
		<p>
			Wir geben bewusst den Medien vor Ort eine Plattform und Sichtbarkeit. Internationale
			Presse/Medien sind leichter zu identifizieren und werden daher nicht extra abgebildet.
		</p>
	</SwiperSlide>
</Swiper>
<h2>
    Unsere Kriterien für die Hintergründe
</h2>
<p>
	Neben den aktuellen News via Twitter wollen wir auch die Arbeit von Journalist*innen im In- und Ausland einbinden. 
	Es gibt verschiedene Plattformen, die Qualitätsjournalismus bündeln und Empfehlungen aussprechen, 
	weswegen wir uns dazu entschieden haben, mit ihnen zusammenzuarbeiten. Desinformation lässt sich vor allem vorbeugen, 
	indem gut recherchierte Inhalte zugänglich gemacht werden.
</p>
<Swiper
	modules={[Pagination]}
	spaceBetween={50}
	autoHeight={true}
	loop
	slidesPerView={1}
	pagination={{ clickable: true }}
    class="mb-5"
>
	<SwiperSlide class="border">
		<h2>1. Transparenz</h2>
		<p>
			Es gibt umfangreiche Informationen zum Medium - Impressum, Kontakt, 
			verantwortliche Personen, Kooperationspartner.
		</p>
	</SwiperSlide>
	<SwiperSlide class="border">
		<h2>2. Erfahrung</h2>
		<p>
			Das Medium arbeitet mit Personen wie Politikwissenschaftler*innen, Journalist*innen, 
			Historiker*innen und/oder, Expert*innen zusammen.
		</p>
	</SwiperSlide>
	<SwiperSlide class="border">
		<h2>3. Kuratierung</h2>
		<p>	
			Das Medium wählt die Beiträge selbst aus oder lässt sie von Personen mit 
			entsprechendem Know-How auswählen.
		</p>
	</SwiperSlide>
</Swiper>
<h2>
    Über die Medien
</h2>
<p>
	<b>piqd</b> arbeitet für eine aufgeklärte und informierte Öffentlichkeit. Ausgewählte Kurator*innen filtern nur wirklich 
	beachtenswerte Inhalte aus dem Netz, empfehlen ihre persönliche und sorgfältig begründete Auswahl und verhelfen 
	so relevanten Beiträgen zu mehr Reichweite. 
</p>
<p>
	<b>KATAPULT</b> visualisiert normalerweise Statistiken und Studien der Sozialwissenschaften, sodass Erkenntnisse 
	schnell und einfach greifbar werden. Seit Beginn des Krieges in der Ukraine fokussiert sich das Team auf die 
	Kriegsberichterstattung und engagiert sich für die Ukrainer*innen. Alle Artikel werden von Wissenschaftler*innen oder Redakteur*innen verfasst. 
</p>
<p>
	Coming soon: <b>The Buzzard</b> bündelt Medienstimmen des ganzen Meinungsspektrums in einer App und ordnet diese journalistisch ein. 
	Die Werte und Prinzipien auf denen Buzzard ihre Arbeit aufbaut sind: Perspektivenvielfalt, Unparteilichkeit, 
	Beteiligung und Mitsprache, konstruktive Debatten, Fokus auf die großen Fragen, Transparenz und werbefreier Journalismus.
</p>
<h2>
    Was können wir noch besser machen?
</h2>
<p>
    Ihr habt Vorschläge für weitere verlässliche Quellen, valide Auswahlkriterien oder andere Verbesserungen dieser Seite, dann schreibt uns gerne!
</p>
<a class="" title="Mail schreiben" href="mailto:info@digital-democracy-alliance.org?subject=FocusOnUkraine">
	Email schreiben
</a>