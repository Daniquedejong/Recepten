<script>
	import Header from '$lib/organisms/header.svelte';
</script>

<Header />

<section>
	<h1>Chinese tomatensoep</h1>
	<p>Chinese tomatensoep combineert de zoete frisheid van tomaten met een vleugje oosterse kruiden. 
        Het is een licht, maar smaakvol gerecht dat vaak wordt geserveerd als voorgerecht in Chinese 
        restaurants. Simpel, hartverwarmend en vol umami!</p>

	<main>
		<article class="ingredienten">
			<label for="personen">Aantal personen: 10</label>
			<h2>Ingrediënten</h2>
			<ul id="ingredienten-lijst">
				<li data-basishoeveelheid="2">Honig chinese tomatensoep: <span class="hoeveelheid">2</span> pakjes</li>
				<li data-basishoeveelheid="500">Pakje gezeefde tomaten: <span class="hoeveelheid">500</span> gram</li>
				<li data-basishoeveelheid="20">Runder soepballetjes: <span class="hoeveelheid">250</span> gram</li>
                <li data-basishoeveelheid="125">Honig krul vermicelli: <span class="hoeveelheid">125</span> gram</li>
                <li data-basishoeveelheid="20">Honig kruidenbuiltje vlees: <span class="hoeveelheid">1</span> zakje</li>
                <li data-basishoeveelheid="20">Maggi bouillon blokje rundvlees: <span class="hoeveelheid">1</span> blokje</li>
			</ul>
		</article>

		<article class="bereiding">
			<h2>Bereiding</h2>
			<h3>
				<b>Stap 1</b><br />
				Doe 3 liter water in een pan en zet op hoog vuur.<br /><br />
				<b>Stap 2</b><br />
				Voeg de twee pakjes chinese tomatensoep, de gezeefde tomaten,
                 het kruidenbuiltje en het bouiilon blokje toe.<br /><br />
				<b>Stap 3</b><br />
				Giet er een klein beetje olijfolie in, zodat het niet aanbrandt. 
                En roer af en toe, anders gaat het klonteren.<br /><br />
				<b>Stap 4</b><br />
				Voeg de krul vermicelli toe en wacht tot het kookt.<br /><br />
                <b>Stap 5</b><br />
				Voeg de soepballetjes toe en laat het ongeveer 10 minuten koken op een middelstandje.<br /><br />
			</h3>
		</article>
	</main>
</section>

<style>
	* {
		box-sizing: border-box;
		margin: 0;
	}

	section {
		background-color: rgb(246, 238, 228);
        color: rgb(63, 123, 80);
		height: auto;
	}

    main {
        font-family: 'Bree serif', helvetica;
        padding: 1em;
    }

	h1 {
		font-family: 'Cinzel', serif;
		display: flex;
		justify-content: center;
		text-align: center;
		margin: 0 auto;
		padding-top: 1.5em;
		font-size: 2.7em;
	}

	p {
		font-family: 'Bree serif', helvetica;
		display: flex;
		justify-content: center;
		font-size: 1.3em;
		max-width: 30em;
		padding: 0.5em;
		text-align: center;
		margin: 0 auto;
		margin-top: 1em;
	}

    .ingredienten h2 {
        margin-top: 1em;
    }

    .ingredienten {
        margin-top: 2em;
        margin-left: 1em;
        background-color: rgb(253, 254, 247);
        padding: 1em;
        border-radius: 1em;
    }

    .bereiding {
        margin-top: 4em;
        margin-left: 1em;
        background-color: rgb(253, 254, 247);
        padding: 1em;
        border-radius: 1em;
    }

	ul {
		list-style-type: none;
		padding: 0;
	}

	li {
		margin: 10px 0;
	}

	h2 {
		font-family: 'Bree serif', helvetica;
		font-weight: 400;
		display: flex;
		margin-bottom: 1em;
	}

	h3 {
		font-family: 'Bree serif', helvetica;
		font-weight: 100;
		font-size: 1em;
	}

	label {
		font-family: 'Bree serif', helvetica;
	}

    /* TABLET MINI */
	@media (min-width: 30em) {
        main {
			margin-top: 5em;
			display: flex;
			justify-content: center;
			gap: 6em;
			margin-left: 1em;
		}
    }

    /* TABLET BIG */
	@media (min-width: 40em) {
        main {
			margin-top: 5em;
			display: flex;
			justify-content: center;
			gap: 10em;
			margin-left: 1em;
		}
    }

      /* DESKTOP SMALL */
	@media (min-width: 50em) {
        main {
			margin-top: 5em;
			display: flex;
			justify-content: center;
			gap: 15em;
			margin-left: 1em;
		}
    }

	/* DESKTOP BIG */
	@media (min-width: 68em) {

        section {
		background-color: rgb(246, 238, 228);
		/* height: 100vh; */
	    }

		h1 {
			font-family: 'Cinzel', serif;
			display: flex;
			justify-content: center;
			padding-top: 1.5em;
			font-size: 4em;
		}

		p {
			font-family: 'Bree serif', helvetica;
			display: flex;
			justify-content: center;
			font-size: 1.3em;
			max-width: 30em;
			text-align: center;
			margin: 0 auto;
			margin-top: 1em;
		}

		main {
			margin-top: 5em;
			display: flex;
			justify-content: center;
			gap: 20em;
			margin-left: 5em;
		}

        .bereiding {
            max-width: 25em;
        }
	}
</style>
