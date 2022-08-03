<script>
	import Section from './Section.svelte'

	const experiences = [
		{
			title: '🎓  Konexio',
			occupation: 'Formateur',
			description:
				"Je suis formateur principal sur un la formation <i>Développeur web et web mobile chez Konexio</i>. La formation est une formation en alternance initiée par un Bootcamp intensif de 3 mois et demi, suivi du cursus alternance pendant 9 mois. Je forme au métier de développeur web fullstack, avec notamment HTML5/CSS3, Javascript, Typescript, Algorithmique, React, Node, Express, SQL, NoSQL, tout en mettant en avant l'accessibilité web et bien sur l'éco-conception.",
			url: 'https://www.konexio.eu/'
		},
		{
			title: '🚸  OpenClassRoom',
			occupation: 'Mentor',
			description:
				"J'accompagne les étudiants durant leur formation de développeur web front-end React, à raison d'une demie heure par semaine. Je partage avec eux les bonnes pratiques du métier, les astuces et les conseils qui vont les aider. Je participe aussi à la préparation et l'élaboration de leur projets et soutenances durant la formation.",
			url: 'https://openclassrooms.com/'
		}
	]
</script>

<Section>
	<h2>Formation</h2>
	<div class="grid">
		{#each experiences as experience}
			<article>
				<div>
					<h3>{experience.title}</h3>
					<span>• {experience.occupation}</span>
					<p>{@html experience.description}</p>
				</div>
				<span>🔗 - <a href={experience.url} target="_blank">{experience.url}</a></span>
			</article>
		{/each}
	</div>
</Section>

<style>
	h2 {
		font-family: 'Raleway-Black';
		font-size: 3rem;
		margin-bottom: 2rem;
	}

	.grid {
		display: grid;
		grid-template-columns: repeat(2, 1fr);
		gap: 2rem;
	}

	article {
		border-radius: 6px;
		box-shadow: 0px 0px 17px -10px rgba(0, 0, 0, 0.2);
		padding: 2rem;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
	}

	h3 {
		font-family: 'Raleway-Bold';
		display: inline;
	}

	p {
		margin: 2rem 0;
		line-height: 1.5rem;
	}

	a {
		color: var(--teal);
		font-family: 'Raleway-Bold';
	}

	@media (max-width: 992px) {
		.grid {
			grid-template-columns: repeat(1, 1fr);
		}
	}

	@media (max-width: 576px) {
		article {
			padding: 1rem;
		}
	}
</style>
