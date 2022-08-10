<script>
	import Section from '$lib/components/Section.svelte'
</script>

<Section>
	<p class="greeting">Hello,</p>
	<span class="greeting">Je suis{` `}</span>
	<h1 class="greeting">Benoit Paquier</h1>
	<span class="greeting">.</span>
	<h2>Formateur & développeur web indépendant</h2>
</Section>

<style>
	h1 {
		display: inline;
	}

	.greeting {
		font-family: 'Raleway-Black', sans-serif;
		font-size: 5rem;
	}

	h2 {
		font-family: 'Raleway-Bold', sans-serif;
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

		h2 {
			font-size: 1.5rem;
		}
	}
</style>
