<script>
	// Import Swiper Svelte components
	import { Swiper, SwiperSlide } from 'swiper/svelte';
	import { Pagination } from 'swiper';

	// Import Swiper styles
	import 'swiper/css';
	import 'swiper/css/pagination';
</script>

<p class="intro">
	Welche Kriterien ziehen wir für die Auswahl der auf Focus on Ukraine hinterlegten Quellen heran?
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
    class="mb-5"
	on:slideChange={() => console.log('slide change')}
	on:swiper={(e) => console.log(e.detail[0])}
>
	<SwiperSlide class="border">
		<h2>1. Transparenz</h2>
		<p>
			Es gibt umfangreiche Informationen zu der Person - wie Herkunft, Ausbildung, Studium,
			Berufserfahrung und Beschäftigung
		</p>
	</SwiperSlide>
	<SwiperSlide class="border">
		<h2>2. Erfahrung</h2>
		<p>
			Die Person hat mehrjährige Erfahrung als Politikwissenschaftler:in, Journalist:in,
			Historiker:in, Expert:in
		</p>
	</SwiperSlide>
	<SwiperSlide class="border">
		<h2>3. Medienzitate</h2>
		<p>Die Person wurde mehrfach von verschiedenen Medien zu dem Thema befragt und/oder zitiert</p>
	</SwiperSlide>
	<SwiperSlide class="border">
		<h2>4. Empfehlungen</h2>
		<p>
			Die Person wurde mehrfach von verschiedenen Medien und/oder Expert:innen zu diesem Thema
			empfohlen.
		</p>
	</SwiperSlide>
	<SwiperSlide class="border">
		<h2>5. Themenfokus</h2>
		<p>
			Der Hauptfokus des Accounts liegt auf dem Thema Russland / Ukraine - aktuelle sowie
			zurückliegende Informationen.
		</p>
	</SwiperSlide>
	<SwiperSlide class="border">
		<h2>6. Medien vor Ort</h2>
		<p>
			Wir geben bewusst den Medien vor Ort eine Plattform und Sichtbarkeit. Internationale
			Presse/Medien sind leichter zu identifizieren und werden daher nicht extra abgebildet.
		</p>
	</SwiperSlide>
</Swiper>
<h2>
    Was können wir noch besser machen?
</h2>
<p>
    Ihr habt Vorschläge für weitere verlässliche Informations-Quellen, valide Auswahlkriterien oder andere Verbesserungen dieser Seite, dann schreibt uns gerne!
</p>
<!-- TODO MAIl -->
<a href="mailto:">
    TODO MAIL ADRESSE EINFÜGEN
</a>