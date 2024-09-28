<script>
    import Header from "$lib/organisms/header.svelte"; 
</script>

<Header />

<section>
	<h1>Italiaans</h1>
	<p>Italiaans eten is een viering van liefde en verse ingrediënten.
         Van knapperige pizza’s tot romige risotto en heerlijke gelato, 
         elke hap brengt je naar de zonnige heuvels van Italië.
          Geniet van de rijke smaken en de gezelligheid aan tafel!</p>

	<main class="container">
		<ul>
			<li><a href="/gerechten/pasta-pesto">Pasta pesto<img src="/assets/pesto.jpg" alt="Italie"/></a></li>
			<li><a href="/">Spaghetti carbonara<img src="/assets/carbonara.jpg" alt="Italie"/></a></li>
			<li><a href="/">Spaghetti bolognese<img src="/assets/bolognese.jpg" alt="Italie"/></a></li>
            <li><a href="/">Lasagna<img src="/assets/bolognese.jpg" alt="Italie"/></a></li>
			<li><a href="/">Plaatpizza<img src="/assets/plaatpizza.jpg" alt="Italie"/></a></li>
			<li><a href="/">Teramisu<img src="/assets/teramisu.jpg" alt="Italie"/></a></li>
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