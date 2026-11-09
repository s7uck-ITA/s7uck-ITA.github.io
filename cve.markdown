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
	.coverflow>section { min-width: 29ch;}
	summary::marker { content: ""; /* LOLLLL*/}
	#interessi summary::marker { content: "\2192";}
	summary h3 { max-width: 71%;}
</style>

<style media="(min-width: 160ch)">
	body>header, body>footer {
		height: 100vh;
		position: sticky;
		top: 0;
	}
	body.horizontal { flex-wrap: nowrap;}
</style>

<style media="(max-width: 920px)">
	main { padding: 1em;}
</style>

<header>
	<img id="myself-mobi" src="/images/iocattedrale.jpg" width=300>

	<h1>{{ site.contact.name }}</h1>
	
	{% include nav.html %}
</header>

<main style="max-width: min(100%, 90ch);">
<div class="snap">
	<h3>Istruzione & Certficazioni</h3>
	<table>{% for row in site.data.curriculum[0].rows %}
		<tr>
			<td>{% if row.h %}<h4>{{ row.h }}</h4>{% endif %}
			{{ row.text }}</td>{% if row.td %}{% for td in row.td %}
			<th class="accent">{{td}}</th>{% endfor %}{% endif %}{% if row.link %}
			<th class="accent"><a href="{{ row.link[1] }}">{{ row.link[0] }}</a></th>{% endif %}
		</tr>{% endfor %}
	</table>
</div>

<div class="snap">
	<h3>Competenze, Skills</h3>
	<section>
		<h3>Informatica</h3>
		<ul class="accordion-ani">
			<details class="section" open>
				<summary><header class="left">
						<a class="clicky button"><img class="icon" src="/images/slide_up.svg"></a>
						<h3>Sistemi operativi</h3>
						</header></summary>
				<table>
					<tr><td>Windows</td></tr>
					<tr><td>GNU/Linux</td></tr>
				</table>
			</details>
			<details class="section">
				<summary><header class="left">
						<a class="clicky button"><img class="icon" src="/images/slide_up.svg"></a>
						<h3>Programmazione e Sviluppo App</h3>
						</header></summary>
				<table>
					<tr><td><a href="https://github.com/{{ site.contact.github }}?tab=repositories&q=&type=&language=python">Python</a></td></tr>
					<tr><td><a href="https://github.com/{{ site.contact.github }}?tab=repositories&q=&type=&language=c%23">C#</a></td></tr>
					<tr><td><a href="https://github.com/{{ site.contact.github }}?tab=repositories&q=&type=&language=javascript">Javascript</a></td></tr>
					<tr><td><a href="https://github.com/s7uck-ITA/s7uck-ITA.github.io/blob/master/_plugins/photo_gen.rb">~Ruby</a></td></tr>
					<tr><td><a href="https://github.com/{{ site.contact.github }}/PowerPage">Windows Forms / Univerasal Windows Platform</a></td></tr>
				</table>
			</details>
			<details class="section">
				<summary><header class="left">
						<a class="clicky button"><img class="icon" src="/images/slide_up.svg"></a>
						<h3>Strumenti informatici</h3>
						</header></summary>
				<table>
					<tr><td><a href="https://github.com/{{ site.contact.github }}">Git</a></td></tr>
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
		<ul class="accordion-ani">
			<details class="section">
				<summary><header class="fully-spaced">
								<h3>Web Design</h3>
								<a class="clicky button"><img src="/images/slide_up.svg"></a>
								</header></summary>
				Costruzione di siti web graficamente avanzati anche solo con HTML e CSS, Apache, express.Js o Jekyll

				<h3>esempi</h3>
				<ul class="scroll coverflow">{% for website in site.showcase %}{% if website.website %}
					<section class="tight">
						<img src="{{ website.image }}" height=200>
						<figcaption>
							<table><tr>
								<td><h4><a href="{{ website.link }}">{{ website.title }}</a></h4></td>
								<th class="accent" onclick="window.location = '{{ website.link }}'"><img class="icon" src="/images/forward.svg"></th>
							</tr></table>
						</figcaption>
					</section>{% endif %}{% endfor %}
				</ul>
			</details>
			<details class="section">
				<summary><header class="fully-spaced">
								<h3>Graphic Design, Progettazione</h3>
								<a class="clicky button"><img class="icon" src="/images/slide_up.svg"></a>
								</header></summary>
				Grafiche promozionali, sfondi, loghi e packaging da zero
			</details>
			<details class="section">
				<summary><header class="fully-spaced">
								<h3>Interface Design e Prototipazione</h3>
								<a class="clicky button"><img class="icon" src="/images/slide_up.svg"></a>
								</header></summary>
				Creo UI Concepts da quando ho memoria, iniziando su PowerPoint, adesso in modo strutturato con Figma e Prototypes. Anche App Windows via uWP
			</details>
		</ul>
	</section>
	<section>
		<h3>Fotografia & Videomaking</h3>
		<ul class="accordion-ani">
			<details class="section" open>
				<summary><header class="left">
						<a class="clicky button"><img class="icon" src="/images/slide_up.svg"></a>
						<h3>Concetti</h3>
						</header></summary>
				<table>
					<tr><td>Regole di composizione</td></tr>
					<tr><td>Scatto manuale</td></tr>
					<tr><td>Elaborazione foto RAW</td></tr>
					<tr><td>L-Cut, jump cut, animazioni</td></tr>
					<tr><td>Node based video editing</td></tr>
				</table>
			</details>
			<details class="section">
				<summary><header class="left">
						<a class="clicky button"><img class="icon" src="/images/slide_up.svg"></a>
						<h3>Software per fotografia</h3>
						</header></summary>
				<table>
					<tr><td>Darktable</td></tr>
					<tr><td>EXIFtool</td></tr>
				</table>
			</details>
			<details class="section">
				<summary><header class="left">
						<a class="clicky button"><img class="icon" src="/images/slide_up.svg"></a>
						<h3>Software per video editing</h3>
						</header></summary>
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
	<ul class="scroll snap coverflow">{% for project in site.showcase %}{% if project.portfolio %}
		<section class="snap{% if project.image %} bg{% endif %}" id="{{ project.slug }}">{% if project.icon %}
			<img class="ily" src="{{ project.icon }}" width=80>{% endif %}
			<header class="fully-spaced nowrap">
			<h3>{{ project.title }}</h3>
			<a class="button" href="{{ project.url }}" title="Altri dettagli"><img class="icon" src="/images/forward.svg"></a>
			</header>
			{{ project.desc }}
		</section>{% endif %}{% endfor %}
	</ul>
</div>

<div class="snap" id="interessi">
	<h3>Alcuni dei miei interessi</h3>
	<ul class="accordion-ani">{% for int in site.data.iluv %}
		<details class="section bg" id="{{ int.id }}">
			<summary><h3>{{ int.title }}</h3></summary>
			{{ int.desc }} 
		</details>{% endfor %}
	</ul>
</div>

<div class="snap">
	<h3>Attività sociali e politiche</h3>
	<table>{% for row in site.data.curriculum[2].rows %}
		<tr>{% if row.years %}
			<td>{{ row.years }}</td>{% endif %}
			<td>{% if row.h %}<h4>{{ row.h }}{% if row.place %} · {{ row.place }}{% endif %}</h4>{% endif %}
			<div>{{ row.text }}</div></td>{% if row.td %}{% for td in row.td %}
			<th class="accent">{{td}}</th>{% endfor %}{% endif %}{% if row.link %}
			<th class="accent"><a href="{{ row.link[1] }}">{{ row.link[0] }}</a></th>{% endif %}
		</tr>{% endfor %}
	</table>
</div>

<div class="snap">
	<h3>Volontariato</h3>
	<table>{% for row in site.data.curriculum[3].rows %}
		<tr>{% if row.years %}
			<td>{{ row.years }}</td>{% endif %}
			<td>{% if row.h %}<h4>{{ row.h }}{% if row.place %} · {{ row.place }}{% endif %}</h4>{% endif %}
			<div>{{ row.text }}</div></td>{% if row.td %}{% for td in row.td %}
			<th class="accent">{{td}}</th>{% endfor %}{% endif %}{% if row.link %}
			<th class="accent"><a href="{{ row.link[1] }}">{{ row.link[0] }}</a></th>{% endif %}
		</tr>{% endfor %}
	</table>
</div>

<div class="snap">
	<h3>Relazionarsi</h3>
	android
</div>

<!--
{% for div in site.data.curriculum %}
<div class="snap">
	<h3>{{ div.title }}</h3>
	{% if div.rows %}<table>{% for row in div.rows %}
		<tr>
			<td>{% if row.h %}<h4>{{ row.h }}</h4>{% endif %}
			<div>{{ row.text }}</div></td>{% if row.td %}{% for td in row.td %}
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
details.bg { background-attachment: fixed;}
{% for int in site.data.iluv %}
.bg#{{ int.id }} { background-image: linear-gradient(#000000bb, #{{ int.color | default: "000000" }}bb), url("{{ int.image }}");}{% endfor %}
{% for prj in site.showcase %}{% if prj.image %}
.bg#{{ prj.slug }} { background-image: linear-gradient(#000000bb, #{{ prj.color | default: "000000" }}bb), url("{{ prj.image }}");}{% endif %}{% endfor %}
</style>