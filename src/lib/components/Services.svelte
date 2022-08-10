<script>
	import Section from '$lib/components/Section.svelte'

	const mainExperiences = [
		{
			title: '🧬 Front-end',
			description: `
        J'utilise <em>React</em> ou <em>Svelte</em> pour développer des sites web.
        J'accorde une importance essentielle à l'accessibilité web et l'eco-conception: deploiement de sites web statiques, optimisation des images, des polices d'écritures, choix du contenu, etc. J'utilise notamment <em>Gatsby</em> avec <em>React</em> ou <em>SvelteKit</em> avec <em>Svelte</em>.
      `
		},
		{
			title: '🔧 Back-end',
			description: `
			  Je travaille principalement avec <em>NodeJS</em> et le framework <em>Express</em>.
        Je développe des <em>API REST</em> ou <em>Graphql</em>, sur lesquelles je travaille avec <em>NoSQL</em> & <em>MongoDB</em> ou <em>SQL</em> & <em>PostgreSQL</em>. Système d'authentification, tâches récurrentes, services, tout ce dont votre application a besoin.
      `
		}
	]

	const secondaryExperiences = [
		{
			title: '🛍️ E-commerce',
			description: `
			  En utilsant <em>Shopify</em> et la <em> Storefront API</em>, je développe des solutions e-commerce sur mesure.
      `
		},
		{
			title: '🌇️ Landing pages',
			description: `
			  En fonction de vos projets, je créé des experiences interactives ou des pages simples qui comblent vos besoin.
      `
		},
		{
			title: '📦 CMS',
			description: `
			  Gérer votre contenu en autonomie est primordial. Je travaille avec les APIs de Wordpress, Strapi ou encore Prismic. 
      `
		}
	]
</script>

<Section>
	<h3>Services</h3>
	<div class="grid-1">
		{#each mainExperiences as experience}
			<article>
				<h4>{experience.title}</h4>
				<p>{@html experience.description}</p>
			</article>
		{/each}
	</div>

	<div class="grid-2">
		{#each secondaryExperiences as experience}
			<article>
				<h4>{experience.title}</h4>
				<p>{@html experience.description}</p>
			</article>
		{/each}
	</div>
</Section>

<style>
	.grid-1 {
		display: grid;
		grid-template-columns: repeat(2, 1fr);
		gap: 2rem;
	}

	.grid-2 {
		margin-top: 2rem;
		display: grid;
		grid-template-columns: repeat(3, 1fr);
		gap: 2rem;
	}

	article {
		border-radius: 6px;
		box-shadow: 0px 0px 17px -10px rgba(0, 0, 0, 0.2);
		padding: 2rem;
	}

	h4 {
		font-family: 'Raleway-Bold', sans-serif;
		display: inline;
	}

	p {
		margin-top: 2rem;
		line-height: 1.5rem;
	}

	@media (max-width: 992px) {
		.grid-1 {
			grid-template-columns: repeat(1, 1fr);
		}

		.grid-2 {
			grid-template-columns: repeat(1, 1fr);
		}
	}

	@media (max-width: 576px) {
		article {
			padding: 1rem;
		}
	}
</style>
