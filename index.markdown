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
	div.leaflet-map {
		height: 650px !important;
		aspect-ratio: 17/14;
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
	{% leaflet_map { "gestureHandling": true } %}
		{% leaflet_marker { "latitude": "40.4712427", "longitude": "17.2432278" } %}
			{%- for post in site.posts -%}
				{% if post.location.geojson %}
					{% leaflet_geojson {{post.location.geojson}} %}
				{% elsif post.location.latitude and post.location.longitude %}
					{% leaflet_marker { "latitude": {{ post.location.latitude }}, "longitude": {{ post.location.longitude }} } %}
				{% endif %}
			{% endfor %}
			{%- for location in site.data.location_map -%}
				{% if location[1].coordinates %}
					{% leaflet_marker {
						"latitude": {{ location[1].coordinates[0] }},
						"longitude": {{ location[1].coordinates[1] }},
						"popupContent": "{{ location[0] }}"
					} %}
				{% endif %}
			{% endfor %}
	{% endleaflet_map %}
</section>
</div>