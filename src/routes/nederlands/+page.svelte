<script>
	import Header from '$lib/organisms/header.svelte';
</script>

<Header />

<section>
	<h1>Nederlands</h1>
	<p>
		Nederlands eten is eenvoudig, maar vol hartige smaken en tradities. Denk aan stamppot,
		erwtensoep en versgebakken brood, vaak geserveerd met kaas of worst. Eten in Nederland
		weerspiegelt de nuchtere cultuur: voedzaam, lekker en gemaakt om van te genieten met familie en
		vrienden. Of het nu een feestelijke haringhapje is of een warme maaltijd op een koude dag, de
		Nederlandse keuken draait om gezelligheid en eenvoud.
	</p>

	<main class="container">
		<ul>
			<li>
				<a href="/gerechten/pasta-pesto"
					>Boerenkool met worst<img src="/assets/boerenkool.webp" alt="Boerenkool" /></a
				>
			</li>
			<li><a href="/">Broccoli met hete kip<img src="/assets/broccoli.jpg" alt="Italie" /></a></li>
			<li><a href="/">Andijvie stamppot<img src="/assets/stampot.jpg" alt="Italie" /></a></li>
			<li><a href="/">Bloemkool<img src="/assets/bloemkool.webp" alt="Italie" /></a></li>
			<li><a href="/">Shuarma bonenschotel<img src="/assets/shuarma.jpeg" alt="Italie" /></a></li>
			<li>
				<a href="/gerechten/chinese-tomatensoep"
					>Chinese tomatensoep<img src="/assets/tomatensoep.jpg" alt="Italie" /></a
				>
			</li>
			<li><a href="/">Pannenkoeken<img src="/assets/pannenkoeken.jpg" alt="Italie" /></a></li>
			<li><a href="/">Poffertjes<img src="/assets/poffertjes.jpg" alt="Italie" /></a></li>
		</ul>
	</main>
</section>

<style>
	* {
		box-sizing: border-box;
		margin: 0;
	}

	section {
		background-color: rgb(246, 238, 228);
	}

	ul {
		list-style: none;
		padding-top: 5em;
		padding-bottom: 5em;
		display: grid;
		gap: 1em;
		grid-template-columns: repeat(auto-fit, minmax(7em, 1fr));
	}

	li {
		font-weight: 800;
		font-size: 1em;
		max-width: 8em;
		padding-top: 2em;
		font-family: 'Cinzel', serif;
	}

	a:hover {
		scale: 1.03;
		transition-duration: 0.3s;
		transition: ease-in-out;
	}

	a {
		text-decoration: none;
		color: rgb(63, 123, 80);
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	a img {
		order: -1;
		margin-left: -1em;
		display: block;
		border-radius: 1em 0em 1em 0em;
		height: 8em;
		width: 8em;
		object-fit: cover;
	}

	h1 {
		font-family: 'Cinzel', serif;
		color: rgb(63, 123, 80);
		display: flex;
		justify-content: center;
		text-align: center;
		margin: 0 auto;
		padding-top: 1.5em;
		font-size: 3em;
	}

	p {
		font-family: 'Bree serif', helvetica;
		color: rgb(63, 123, 80);
		display: flex;
		justify-content: center;
		font-size: 1.3em;
		max-width: 30em;
		padding: 0.5em;
		text-align: center;
		margin: 0 auto;
		margin-top: 1em;
	}

	/* MOBILE NORMAL */
	@media (min-width: 24em) {
		ul {
			grid-template-columns: repeat(auto-fit, minmax(10em, 1fr));
		}

		li {
			font-size: 1.1em;
		}

		a img {
			height: 9em;
			width: 9em;
		}
	}

	/* MOBILE NORMAL glitch */
	@media (min-width: 24em) and (max-width: 34.5em) {
		ul li a img {
			margin-left: -0.25em;
		}
	}

	/* DESKTOP */
	@media (min-width: 68em) {
		ul {
			grid-template-columns: repeat(auto-fit, minmax(20em, 1fr));
		}

		li {
			font-size: 2.3em;
		}

		a img {
			height: 8em;
			width: 8em;
			margin-left: 1em;
		}

		h1 {
			font-size: 4em;
		}
	}
</style>
