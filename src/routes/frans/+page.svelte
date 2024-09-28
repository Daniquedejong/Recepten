<script>
    import Header from "$lib/organisms/header.svelte"; 
</script>

<Header />

<section>
	<h1>Frans</h1>
	<p>Frans eten is een symfonie van smaken, finesse en traditie. 
        Het staat bekend om zijn uitstekende technieken en hoogwaardige ingrediënten, 
        van verse baguettes en romige kaas tot verfijnde gerechten zoals coq au vin en ratatouille. 
        Eten in Frankrijk is vaak een kunstvorm, waarbij maaltijden worden genoten als 
        sociale gebeurtenissen, compleet met goede wijnen en uitgebreid tafelen. 
        De Franse keuken weerspiegelt een rijke culinaire geschiedenis en een liefde voor het goede leven, 
        waar elke hap een moment van genot is.</p>

          <main class="container">
            <ul>
                <li><a href="/gerechten/pasta-pesto">Boeuf Bourguignon<img src="/assets/boeuf.jpg" alt="Italie"/></a></li>
                <li><a href="/">Draadjesvlees<img src="/assets/draadjesvlees.png" alt="Italie"/></a></li>
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
