<script>
	import Section from './Section.svelte'
</script>

<Section>
	<p class="greeting">Hello,</p>
	<span class="greeting">Je suis{` `}</span>
	<h1 class="greeting">Benoit Paquier</h1>
	<span class="greeting">.</span>
	<h3>Formateur & développeur web indépendant</h3>
</Section>

<style>
	h1 {
		display: inline;
	}

	.greeting {
		font-family: 'Raleway-Black';
		font-size: 5rem;
	}

	h3 {
		font-family: 'Raleway-Bold';
		font-size: 2rem;
		margin-top: 1rem;
	}

	@media (max-width: 992px) {
		.greeting {
			font-size: 4rem;
		}
	}

	@media (max-width: 576px) {
		.greeting {
			font-size: 3rem;
		}

		h3 {
			font-size: 1.5rem;
		}
	}
</style>
