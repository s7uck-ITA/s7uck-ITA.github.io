---
layout: default
---

<style>
	html { scroll-snap-type: y proximity;}
	body>.snap {
		padding: 5vw;
		min-height: 29vh;
	}
	.hero { overflow: hidden;}
	#myself-mobi {
		aspect-ratio: 1;
		border: 15px double #bdf6b2;
		object-position: right;
	}
	div.leaflet-map {
		height: 650px !important;
		aspect-ratio: 17/14;
	}
</style>

<div class="snap">
<header>
	<img id="myself-mobi" src="/images/20221030_170034.jpg" width=200>

	<h1>{{ site.contact.name }}</h1>
	
	{% include nav.html %}
</header>

<main class="gridlock ani">
	<section class="center">
		<menu>
			<li><a href="mailto:{{ site.contact.email }}">{{ site.contact.email | replace: "@", " [chiocciola] "}}</a></li>
		</menu>
	</section>
	<section>
		<table>{% for contact in site.contact %}
			<tr>
				<td>{{ contact[0] }}</td>
				<td>{{ contact[1] }}</td>
			</tr>{% endfor %}
		</table>
	</section>
</main>
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