---
layout: default
class: horizontal
permalink: /cve
---

<style>
	html { scroll-snap-type: y proximity;}
	/*body { max-width: unset;}*/
	main { flex-direction: column;}
	main>.snap {
		padding: 5vw 0;
		min-height: 29vh;
	}
	#myself-mobi {
		aspect-ratio: 1;
		border: 15px double #bdf6b2;
		object-position: right;
	}
</style>

<style media="(min-width: 920px)">
	body>header, body>footer {
		height: 100vh;
		position: sticky;
		top: 0;
	}
	body.horizontal { flex-wrap: nowrap;}
</style>

<header>
	<img id="myself-mobi" src="/images/iocattedrale.jpg" width=300>

	<h1>{{ site.contact.name }}</h1>
	
	{% include nav.html %}
</header>

<main>
<div class="snap">
<section class="horizontal nowrap" style="background-color: #696932">
	<h2>(!)</h2>
	Questa pagina è in costruzione e contiene riferimenti personali, ancora da filtrare. È vietata la riproduzione.
</section>
</div>

<div class="snap">
	<h3>Istruzione & Certficazioni</h3>
	<table>
		<tr>
			<td><h4>Diploma di maturità scientifica</h4>
			Liceo "Giuseppe Moscati" di Grottaglie: indirizzo scienze applicate</td>
			<th class="accent">100/100</th>
		</tr>
		<tr>
			<td><h4>Certificazione linguistica</h4>
			Cambridge English FIRST</td>
			<th class="accent">C1</th>
		</tr>
		<tr>
			<td><h4>Patente di guida</h4>
			0 errori.</td>
			<th class="accent">B</th>
		</tr>
	</table>
</div>

<div class="snap">
	<h3>Competenze, Skills</h3>
	<section>
		<h3>Informatica</h3>
		<ul class="scroll coverflow">
			<!-- questi dovrebbero essere details -->
			<section>
				<h3>Sistemi operativi</h3>
				<table>
					<tr><td>Windows</td></tr>
					<tr><td>GNU/Linux</td></tr>
				</table>
			</section>
			<section>
				<h3>Programmazione</h3>
				<table>
					<tr><td>Python</td></tr>
					<tr><td>C#</td></tr>
					<tr><td>Javascript</td></tr>
				</table>
			</section>
			<section>
				<h3>Strumenti informatici</h3>
				<table>
					<tr><td>Microsoft Office</td></tr>
					<tr><td>Libreoffice</td></tr>
					<tr><td>SQL</td></tr>
					<tr><td>Shell Scripting e Automazione</td></tr>
				</table>
			</section>
		</ul>
	</section>
	<section>
		<h3>Design & Grafica</h3>
		<ul class="scroll coverflow">
			<section>
				<h3>Web Design</h3>
			</section>
			<section>
				<h3>Graphic Design, Progettazione</h3>
			</section>
			<section>
				<h3>Interface Design e Prototipazione</h3>
			</section>
		</ul>
	</section>
	<section>
		<h3>Fotografia & Videomaking</h3>
		<ul class="scroll coverflow">
			<section>
				<h3>Concetti</h3>
			</section>
			<section>
				<h3>Software per fotografia</h3>
			</section>
			<section>
				<h3>Software per video editing</h3>
			</section>
		</ul>
	</section>
	<section>
		<h3>test cards</h3>
		<ul class="scroll coverflow">
			<section>
				<img class="ily" src="https://upload.wikimedia.org/wikipedia/commons/b/b0/Openstreetmap_logo.svg" width=80>
				<header class="fully-spaced horizontal">
				<h3>OpenStreetMap</h3>
				<a class="button">Altri dettagli</a>
				</header>
				OpenStreetMap è una mappa del mondo libera all'uso e apertamente modiﬁcabile. Dal 2025 modifico assiduamente la mappa tentando il più possibile di completarla con ciò che
				conosco della mia zona.
			</section>
		</ul>
	</section>
</div>

<div class="snap">
	<h3>Dimensioni di me</h3>
	<ul class="scroll coverflow">
		<section>
			<h3>Tecnologia e Informatica</h3>
			Ho imparato da autodidatta negli anni a usare professionalmente il computer per
			programmazione, graﬁca, video editing e creazione siti web.
		</section>
		<section>
			<h3>Fotografia</h3>
			Sono da lungo tempo appassionato di fotografia. Mi piace catturare in particolar modo paesaggi, ma anche scatti più avanzati come quelli al cielo notturno.
		</section>
		<section>
			<h3>Cultura e Conoscenza del mondo</h3>
			Intendo comprendere a fondo i meccanismi che regolano le nostre società. Ho
			approfondito già da prima delle superiori dei temi di economia, e successivamente ho
			maturato interesse per tutto ciò che riguarda la geopolitica, la storia, la comunicazione e
			l'espressione culturale dei singoli individui e dei popoli. Mi appassionano, ad esempio, la
			musica, l'architettura e la letteratura.
		</section>
	</ul>
</div>

<div class="snap">
	<h3>Attività sociali e politiche</h3>
	<table>
		<tr>
			<td>2026</td>
			<td><h4>Premio "Alessandro Leogrande" · Taranto</h4>
			Il premio "Alessandro Leogrande", intitolato a un giornalista mio concittadino scomparso
			nel 2017, è un premio rilasciato su base annuale a libri di giornalismo narrativo.
			Quest'anno ho partecipato alla votazione leggendo "Quando il mondo dorme" di
			Francesca Albanese, relatrice ONU per la questione palestinese, e ho contribuito nel mio piccolo alla sua premiazione.</td>
			<th class="accent"><a>Altri dettagli</a></th>
		</tr>
		<tr>
			<td>2017</td>
			<td><h4>AEDE - Ambasciatori d'Europa 2018 · Ceglie Messapica</h4>
			Primo premio "Giuseppe Tramarollo" scuole primarie e attestato di merito eccezionale.
			L'obiettivo del concorso era immaginare un percorso attraverso il quale potesse
			realizzarsi una vera unione europea. Ho partecipato presentando il logo e il video promo,
			in lingua inglese, di un'ipotetica tv europea "eu 1 tv" con palinsesti che incentivassero nei
			cittadini un sentimento di appartenenza e fratellanza europea.</td>
			<th class="accent"><a>Altri dettagli</a></th>
		</tr>
	</table>
</div>

<div class="snap">
	<h3>Volontariato</h3>
	<table>
		<tr>
			<td>6/2025</td>
			<td><h4>3ª Passeggiata di Solidarietà</h4>
			Passeggiata di 4 km a sostegno del reparto di Oncoematologia Pediatrica a Taranto, con
			destinazione Aeroporto di Grottaglie.</td>
		</tr>
		<tr>
			<td>9/2025+</td>
			<td><h4>OpenStreetMap</h4>
			OpenStreetMap è una mappa del mondo libera all'uso e apertamente modiﬁcabile. Dal
			2025 modifico assiduamente la mappa tentando il più possibile di completarla con ciò che
			conosco della mia zona.</td>
			<th class="accent"><a>Altri dettagli</a></th>
		</tr>
		<tr>
			<td>3/2026</td>
			<td><h4>Iscrizione a ADMO (Associazione Donatori di Midollo Osseo)</h4></td>
		</tr>
	</table>
</div>

<div class="snap">
	<h3>Relazionarsi</h3>
</div>

<!--
{% for div in site.data.curriculum %}
<div class="snap">
	<h3>{{ div.title }}</h3>
	{% if div.rows %}<table>{% for row in div.rows %}
		<tr>
			<td>{% if row.h %}<h4>{{ row.h }}</h4>{% endif %}
			{{ row.text }}</td>{% if row.td %}{% for td in row.td %}
			<th class="accent">{{td}}</th>{% endfor %}{% endif %}{% if row.link %}
			<th class="accent"><a href="{{ row.link[1] }}">{{ row.link[0] }}</a></th>{% endif %}
		</tr>{% endfor %}
	</table>{% endif %}
</div>
{% endfor %}
-->
</main>

<!--footer>
	<nav>
		<menu class="vertical">
			<li>ciao</li>
			<li>ciao</li>
			<li>ciao</li>
			<li>ciao</li>
			<li>ciao</li>
			<li>ciao</li>
		</menu>
	</nav>
</footer-->