<script>
	import Container from './Container.svelte'
	import Section from './Section.svelte'
</script>

<div>
	<Container>
		<Section>
			<h3>Contact</h3>
		</Section>
	</Container>
</div>

<style>
	div {
		background-color: var(--darkBlue);
		color: white;
	}

	h3 {
		font-family: 'Raleway-Black', sans-serif;
		font-size: 3rem;
		margin-bottom: 2rem;
	}
</style>
