---
layout: default
class: ani
---

<style>
	html { scroll-snap-type: y proximity;}
	body>.snap { padding: 14vh 5vw;}
	.hero { overflow: hidden;}
	#myself-mobi {
		aspect-ratio: 1;
		position: absolute;
		bottom: -21%;
		left: 5%;
		border: 15px double #bdf6b2;
	}
</style>

<div class="snap">
<header class="hero">
	<img id="myself-mobi" src="/images/Wallpaper_04.jpg" width=200>

	<h1 class="hero">{{ site.title }}</h1>
</header>
<!--section class="center">
	<nav><menu>
		<li>links out</li>
		<li style=""></li>
		<li>scendi</li>
	</menu></nav>
</section-->
<main class="gridlock">
	<section class="center">
		<h2>Chi sono?</h2>
		<p>Sono uno studente di 18 anni dal Sud Italia e questo è il mio sito web</p>
	</section>
</main>
</div>

<div class="snap">
<main class="gridlock ani">
	<section>
		<h3>Che faccio</h3>
		<p>Oltre a studiare [inserisci facoltà qui] a [inserisci ateneo qui], mi dedico ai miei interessi&hellip;</p>
	</section>
	<section>
		<h3>Cosa mi piace?</h3>
		<p>seconda sezione</p>
	</section>
	<section>
		<h3>Cosa puoi trovare su questo sito?</h3>
		{% include nav.html %}
	</section>
</main>
</div>

{% assign last_few_photos = site.pages | where_exp: "item", "item.dir contains site.photos.output_url" | sort: "date" | reverse | slice: 0, 8 %}
<div class="snap">
<section>
	<header class="fully-spaced horizontal">
		<h2>ultime foto</h2>
		<menu>
			<li><a href="/gallery"><img class="icon" src="/images/camera.svg"> tutte le foto</a></li>
		</menu>
	</header>
	<div class="ani flex flexlock nowrap full-width scroll snap" style="background-color: black">{% for photo in last_few_photos %}
		<img src="{{ photo.image }}" alt="{{ photo.title | default: photo.filename }}" onclick="window.location = '{{ photo.url }}'" title="{{ photo.filename }}" class="section snap" height=350>{% endfor %}
	</div>
</section>
</div>

<div class="snap">
<section>
	<iframe width="425" src="https://www.openstreetmap.org/export/embed?bbox=-312.18750000000006%2C-83.8299454239804%2C312.18750000000006%2C83.82994542398042&amp;layer=mapnik" style="width: 100%; aspect-ratio: 425/350"></iframe><br/><small><a href="https://www.openstreetmap.org/#map=2/0.0/0.0">Visualizza mappa ingrandita</a></small>
</section>
</div>