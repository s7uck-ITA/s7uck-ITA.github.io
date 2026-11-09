---
layout: default
class: aniii
---

{% assign last_song = site.posts | where_exp: "item", "item.track" | first %}
{% assign track_recency_limit = "now" | date: "%s" | minus: 1209600 | date: "%Y%m%d" %} <!-- 2 weeks -->
{% assign song_date = last_song.date | date: "%Y%m%d" %}

<style>
	html { scroll-snap-type: y proximity;}
	body>.snap {
		padding: 5vw;
		min-height: 29vh;
	}
	.hero { overflow: hidden;}
	#myself-mobi {
		aspect-ratio: 1;
		position: absolute;
		bottom: -21%;
		left: 5%;
		border: 15px double #bdf6b2;
		object-position: right;
	}
	#albumart {
		max-height: 70px;
		position: absolute;
		right: 2em;
		top: -2em;
		border: 2px solid aliceblue;
		z-index: -1;
	}
	button:hover>#albumart { rotate: 3deg; top: -2.5em;}
	div.leaflet-map {
		height: 650px !important;
		aspect-ratio: 17/14;
	}
</style>

<div class="snap">
<header class="hero">
	<img id="myself-mobi" src="/images/20221030_170034.jpg" width=200>

	<h1 class="hero">{{ site.title }}</h1>
</header>
<main class="gridlock ani">
	<section class="center">
		<p>Sono un giovane studente salentino e questo è il mio spazio su Internet.</p>
	</section>{% if last_song and song_date >= track_recency_limit %}
	<section>
		<h3>Canzone in l&infin;p</h3>
		<button class="ily" onclick="window.location = '{{ last_song.url }}'">
			<img src="{{ last_song.track.cover }}" id="albumart"> 
			<img class="icon" src="/images/music.svg"> 
			<b>{{ last_song.track.name }}</b> · {{ last_song.track.artists | join: ', ' }}
		</button>
	</section>{% endif %}
</main>
</div>

<div class="snap">
<section>
	<header class="fully-spaced horizontal">
		<h2>esplora il sito</h2>
		{% include nav.html ani="yes" %}
	</header>
	<ul class="ani coverflow stretch">{% for item in site.posts limit:7 %}
		<section class="tight" onclick="window.location = '{{ item.url }}'">{% if item.image %}
			<img src="{{ item.image }}" height=200>{% elsif item.track.cover %}<img src="{{ item.track.cover }}" height=200>{% endif %}
			<figcaption>
				<table>{% unless item.notitle %}
					<thead><th colspan="3"><big>{{ item.title }}</big></th></thead>{% endunless %}
					<tr>{% if item.notitle %}
						<td class="ily">
							{% if item.track %}<img class="icon" src="/images/music.svg" alt="Music"> <b>Canzone</b>{% else %}<b>Post</b>{% endif %} del
						</td>{% endif %}
						<td class="timestamp"><time>{{ item.date | date: "%-d %b, %Y" }}</time></td>{% if item.location %}
						<td class="ily"><img class="icon" src="/images/location.svg" alt="Location">
							{{ item.location }}
						</td>{% endif %}
					</tr>
				</table>
			</figcaption>
		</section>{% endfor %}
	</ul>
</section>
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
	<ul class="ani full-width scroll snap coverflow">{% for photo in last_few_photos %}
		<img src="{{ photo.image }}" alt="{{ photo.title | default: photo.filename }}" onclick="window.location = '{{ photo.url }}'" title="{{ photo.filename }}" class="section snap" height=350>{% endfor %}
	</ul>
</section>
</div>

<footer class="snap">
	<a class="button accent" href="/2026/09/06/example.html">(example)</a>
</footer>

<!--div class="snap">
<section>
	leaflet_map { "gestureHandling": true } %
		% leaflet_marker { "latitude": "40.4712427", "longitude": "17.2432278" } %
			%- for post in site.posts -%
				% if post.location.geojson %
					% leaflet_geojson {{post.location.geojson}} %
				% elsif post.location.latitude and post.location.longitude %
					% leaflet_marker { "latitude": {{ post.location.latitude }}, "longitude": {{ post.location.longitude }} } %
				% endif %
			% endfor %
			%- for location in site.data.location_map -%
				% if location[1].coordinates %
					% leaflet_marker {
						"latitude": {{ location[1].coordinates[0] }},
						"longitude": {{ location[1].coordinates[1] }},
						"popupContent": "{{ location[0] }}"
					} %
				% endif %
			% endfor %
	% endleaflet_map %
</section>
</div-->