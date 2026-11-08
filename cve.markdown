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
		max-width: 100%;
	}
	#myself-mobi {
		aspect-ratio: 1;
		border: 15px double #bdf6b2;
		object-position: right;
	}
	section { overflow: auto;}
	.coverflow>section {
		min-width: 29ch;
	}
	summary::marker {
		content: ""; /*LOLLLL*/
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

<main style="max-width: 100%;">
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
			0 errori</td>
			<th class="accent">B</th>
		</tr>
	</table>
</div>

<div class="snap">
	<h3>Competenze, Skills</h3>
	<section>
		<h3>Informatica</h3>
		<ul>
			<details class="section" open>
				<summary><h3>Sistemi operativi</h3></summary>
				<table>
					<tr><td>Windows</td></tr>
					<tr><td>GNU/Linux</td></tr>
				</table>
			</details>
			<details class="section">
				<summary><h3>Programmazione</h3></summary>
				Dallo scripting ad intere applicazioni server & client side
				<table>
					<tr><td>Python</td></tr>
					<tr><td>C#</td></tr>
					<tr><td>Javascript</td></tr>
					<tr><td>~Ruby</td></tr>
				</table>
			</details>
			<details class="section">
				<summary><h3>Strumenti informatici</h3></summary>
				<table>
					<tr><td>Git</td></tr>
					<tr><td>Microsoft Office</td></tr>
					<tr><td>Libreoffice</td></tr>
					<tr><td>SQL</td></tr>
					<tr><td>Shell Scripting e Automazione / CI-CD</td></tr>
					<tr><td>Sublime Text</td></tr>
				</table>
			</details>
		</ul>
	</section>
	<section>
		<h3>Design & Grafica</h3>
		<ul>
			<details class="section">
				<summary><header class="fully-spaced">
								<h3>Web Design</h3>
								<a class="button">esempi</a>
								</header></summary>
				Costruzione di siti web graficamente avanzati anche solo con HTML e CSS, Apache, express.Js o Jekyll
			</details>
			<details class="section">
				<summary><header class="fully-spaced">
								<h3>Graphic Design, Progettazione</h3>
								<a class="button">esempi</a>
								</header></summary>
				Grafiche promozionali, sfondi, loghi e packaging da zero
			</details>
			<details class="section">
				<summary><header class="fully-spaced">
								<h3>Interface Design e Prototipazione</h3>
								<a class="button">esempi</a>
								</header></summary>
				Creo UI Concepts da quando ho memoria, iniziando su PowerPoint, adesso in modo strutturato con Figma e Prototypes. Anche App Windows via uWP
			</details>
		</ul>
	</section>
	<section>
		<h3>Fotografia & Videomaking</h3>
		<ul>
			<details class="section" open>
				<summary><h3>Concetti</h3></summary>
				<table>
					<tr><td>Regole di composizione</td></tr>
					<tr><td>Scatto manuale</td></tr>
					<tr><td>Elaborazione foto RAW</td></tr>
					<tr><td>L-Cut, jump cut, animazioni</td></tr>
					<tr><td>Node based video editing</td></tr>
				</table>
			</details>
			<details class="section">
				<summary><h3>Software per fotografia</h3></summary>
				<table>
					<tr><td>Darktable</td></tr>
					<tr><td>EXIFtool</td></tr>
				</table>
			</details>
			<details class="section">
				<summary><h3>Software per video editing</h3></summary>
				<table>
					<tr><td>VSDC Video Editor</td></tr>
					<tr><td>Olive</td></tr>
					<tr><td>Kdenlive</td></tr>
					<tr><td>FFmpeg</td></tr>
				</table>
			</details>
		</ul>
	</section>
</div>

<div class="snap">
	<h3>Portfolio</h3>
	<ul class="scroll coverflow">
		<section>
			<img class="ily" src="https://upload.wikimedia.org/wikipedia/commons/b/b0/Openstreetmap_logo.svg" width=80>
			<header class="fully-spaced">
			<h3>OpenStreetMap</h3>
			<a class="button" href="/showcase/osm.html">Altri dettagli</a>
			</header>
			OpenStreetMap è una mappa del mondo libera all'uso e apertamente modiﬁcabile. Dal 2025 modifico assiduamente la mappa tentando il più possibile di completarla con ciò che
			conosco della mia zona.
		</section>
		<section>
			<header class="fully-spaced">
			<h3>Special UX</h3>
			<a class="button">Altri dettagli</a>
			</header>
			Il mio concept UI più dettagliato e serimentale. È pensato da zero per essere prevedibile e innovativo al tempo stesso.
		</section>
	</ul>
</div>

<div class="snap">
	<h3>Dimensioni di me</h3>
	<ul>
		<details class="section bg" id="av">
			<summary><h3>Aviazione</h3></summary>
			Tutto ciò che vola fa i miei sogni fin da quando ero piccolo. 
		</details>
		<details class="section bg" id="tech">
			<summary><h3>Tecnologia e Informatica</h3></summary>
			Ho imparato da autodidatta negli anni a usare professionalmente il computer per
			programmazione, graﬁca, video editing e creazione siti web.
		</details>
		<details class="section bg" id="photo">
			<summary><h3>Fotografia</h3></summary>
			Sono da lungo tempo appassionato di fotografia. Mi piace catturare in particolar modo paesaggi, ma anche scatti più avanzati come quelli al cielo notturno.
		</details>
		<details class="section bg" id="design">
			<summary><h3>Design</h3></summary>
			Disegnare e “immaginare cose” mi permette di dare sfogo a una creatività interiore, che mi spinge a ripensare esteticamente o tecnicamente ciò che uso. Diversi anni fa mi sono avvicinato al graphic design, e successivamente all’interface design, product design, web design, e in generale al design artistico e tecnico (anche interior, urban, transport etc).
			<br><br>Il design è il mezzo dell'interazione tra umano e strumento, o umano e ambiente. Dev'essere quindi in un certo senso “stoico” rispetto all’utente, ma contemporaneamente consapevole del fine dell'oggetto o del sistema: cioè il design richiede attenzione e lungimiranza oltre che un buon senso estetico. Ho iniziato da piccolo a creare concept di sistemi operativi, pagine web semplici imparando l’HTML e il CSS, e occasionalmente grafiche promozionali come locandine o banner. Con il tempo ho affinato molto questa abilità, a partire da nozioni tecniche, per poi arrivare a creare design originali partendo da concetti nuovi.
		</details>
		<details class="section bg" id="mutset">
			<summary><h3>Musica</h3></summary>
			Ho iniziato ad interessarmi attivamente di musica solo da pochi anni, esplorando cioè dei generi, e provando a produrre qualcosa. In termini di gusti musicali non sono molto originale per la mia età. Ascolto perlopiù rap e hip hop, mentre per la musica strumentale, techno e house tra le altre cose.<br>Molti giudicano la musica della mia generazione come superficiale, ma non è così, infatti tra i miei artisti preferiti figurano delle penne che fanno invidia anche ad artisti internazionali. Come ogni corrente artistica se ne può dire di tutto, ma comunque si studierà nei libri di scuola.
		</details>
		<details class="section bg" id="world">
			<summary><h3>Cultura e Conoscenza del mondo</h3></summary>
			Intendo comprendere a fondo i meccanismi che regolano le nostre società. Ho
			approfondito già da prima delle superiori dei temi di economia, e successivamente ho
			maturato interesse per tutto ciò che riguarda la geopolitica, la storia, la comunicazione e
			l'espressione culturale dei singoli individui e dei popoli. Mi appassionano, ad esempio, la
			musica, l'architettura e la letteratura.
		</details>
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
			<th class="accent"><a href="/showcase/leogrande.html">Altri dettagli</a></th>
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
			<th class="accent"><a href="/showcase/osm.html">Altri dettagli</a></th>
		</tr>
		<tr>
			<td>3/2026</td>
			<td><h4>Iscrizione a ADMO (Associazione Donatori di Midollo Osseo)</h4></td>
			<th class="accent"><a href="https://admo.it/">Altri dettagli</a></th>
		</tr>
	</table>
</div>

<div class="snap">
	<h3>Relazionarsi</h3>
	android
	<table>
		<th><h3>i miei difetti</h3></th>
		<tr><td></td></tr>
	</table>
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

<style>
details.bg {
	background-attachment: fixed;
	background-size: cover;
}
.bg#av { background-image: linear-gradient(#000b, #22cb), url(/images/interes/Av.JPG);}
.bg#design { background-image: linear-gradient(#000b, #4a5b), url(/images/interes/kino.jpg);}
.bg#tech { background-image: linear-gradient(#000b, #4a5b), url();}
.bg#photo { background-image: linear-gradient(#000b, #441b), url(/images/interes/camera.webp);}
.bg#mutset { background-image: linear-gradient(#000b, #4a5b), url(/images/interes/kino.jpg);}
.bg#world { background-image: linear-gradient(#000b, #299b), url(/images/interes/world.jpg);}
</style>