<script>
	import { onMount } from 'svelte';
	import Header from '$lib/organisms/header.svelte';

	onMount(() => {
		const personenInput = document.getElementById('personen');
		const minusButton = document.getElementById('minus');
		const plusButton = document.getElementById('plus');

		function updateIngredienten() {
			const aantalPersonen = personenInput.value;
			const ingredientenLijst = document.querySelectorAll('#ingredienten-lijst li');

			ingredientenLijst.forEach(function (item) {
				const basisHoeveelheid = item.getAttribute('data-basishoeveelheid');
				const nieuweHoeveelheid = (basisHoeveelheid * aantalPersonen) / 2; // Aangepast voor 2 personen
				item.querySelector('.hoeveelheid').textContent = nieuweHoeveelheid.toFixed(0);
			});
		}

		personenInput.addEventListener('input', updateIngredienten);

		minusButton.addEventListener('click', () => {
			let currentValue = parseInt(personenInput.value);
			if (currentValue > 1) {
				personenInput.value = currentValue - 1;
				updateIngredienten();
			}
		});

		plusButton.addEventListener('click', () => {
			let currentValue = parseInt(personenInput.value);
			personenInput.value = currentValue + 1;
			updateIngredienten();
		});
	});
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
			<!-- <div class="button-container">
				<button id="minus" class="button">-</button>
				<input type="number" id="personen" value="2" min="1" />
				<button id="plus" class="button">+</button>
			</div> -->

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
				Doe 3 liter water in een pan en zet op hoog vuur.<br />
				<b>Stap 2</b><br />
				Voeg de twee pakjes chinese tomatensoep, de gezeefde tomaten,
                 het kruidenbuiltje en het bouiilon blokje toe.<br />
				<b>Stap 3</b><br />
				Giet er een klein beetje olijfolie in, zodat het niet aanbrandt. 
                En roer af en toe, anders gaat het klonteren.<br />
				<b>Stap 4</b><br />
				Voeg de krul vermicelli toe en wacht tot het kookt.<br />
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
		font-size: 3em;
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

    .ingredienten {
        margin-top: 2em;
        margin-left: 1em;
    }

    .bereiding {
        margin-top: 4em;
        margin-left: 1em;
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

	.button-container {
		display: flex;
		align-items: center;
		/* justify-content: center; */
		gap: 10px;
	}

	.button {
		background-color: rgb(63, 123, 80);
		color: white;
		border: none;
		border-radius: 5px;
		padding: 1px 8px;
		font-size: 1.1em;
		cursor: pointer;
		transition: background-color 0.3s ease;
	}

	.button:hover {
		background-color: rgb(45, 90, 58);
	}

	input[type='number'] {
		-moz-appearance: textfield; /* Verberg pijltjes in Firefox */
	}

	input[type='number']::-webkit-inner-spin-button,
	input[type='number']::-webkit-outer-spin-button {
		-webkit-appearance: none; /* Verberg pijltjes in Chrome/Safari */
		margin: 0; 
	}

	input[type='number'] {
		width: 50px;
		text-align: center;
		font-size: 1em;
		border: 1px solid rgb(63, 123, 80);
		border-radius: 5px;
		appearance: none;
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
