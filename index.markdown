---
layout: default
---

<style>
	html { scroll-snap-type: y mandatory;}
	.snap { padding: 20vh 1vw;}
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
	<img id="myself-mobi" src="/images/me.JPG" width=200>

	<h1 class="hero">{{ site.title }}</h1>
</header>
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

<div class="snap">
<main class="gridlock">
	<section>
		<h2>ultime foto</h2>
	</section>
</main>
</div>

<div class="snap">
<main class="gridlock">
	<section>
		<h2>mappa</h2>
	</section>
</main>
</div>