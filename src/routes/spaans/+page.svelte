<script>
    import Header from "$lib/organisms/header.svelte"; 
</script>

<Header />

<section>
	<h1>Spaans</h1>
	<p>Spaans eten is een feest van smaken en levendige tradities. 
        Van tapas tot paella, het draait om het delen van kleine 
        gerechten en genieten met vrienden en familie. 
        De Spaanse keuken maakt volop gebruik van verse ingrediënten zoals olijfolie, 
        tomaten en zeevruchten, met regionale specialiteiten die het land rijk maken. 
        Eten in Spanje is niet alleen een maaltijd, maar een sociaal ritueel, 
        vaak begeleid door goede wijn en eindeloos gezellige gesprekken.</p>

	<main class="container">
		<ul>
			<li>
				<a href="/gerechten/pasta-pesto">Tortillas<img src="/assets/pasta-pesto.jpg" alt="Italie"/></a>
			</li>
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
		grid-template-columns: repeat(auto-fit, minmax(20em, 1fr));
	}

	li {
		font-weight: 800;
		font-size: 2.3em;
		padding-top: 2em;
		font-family: 'Cinzel', serif;
	}

    a:hover {
        scale: 1.03;
        transition-duration: .3s;
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
        border-radius: 4em 4em 0em 0em;
        height: 8em;
		width: 8em;
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
        font-family: "Bree serif", helvetica;
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

    /* DESKTOP */
 @media (min-width: 68em) {

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
		grid-template-columns: repeat(auto-fit, minmax(20em, 1fr));
	}

	li {
		font-weight: 800;
		font-size: 2.3em;
		padding-top: 2em;
		font-family: 'Cinzel', serif;
	}

    a:hover {
        scale: 1.03;
        transition-duration: .3s;
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
		display: block;
		width: 50%;
        border-radius: 1em 0em 1em 0em;
        height: 8em;
		width: 8em;
        object-fit: cover;
	}

    h1 {
        font-family: 'Cinzel', serif;
        display: flex;
        justify-content: center;
        padding-top: 1.5em;
        font-size: 4em; 
    }

    p {
        font-family: "Bree serif", helvetica;
        display: flex;
        justify-content: center;
        font-size: 1.3em;
        max-width: 30em;
        text-align: center;
        margin: 0 auto;
        margin-top: 1em;
    }
 }

 </style>