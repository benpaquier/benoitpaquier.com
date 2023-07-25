<script>
	import Container from '$lib/components/Container.svelte'
	import Contact from '$lib/components/Contact.svelte'
	import Hero from '$lib/components/Hero.svelte'
	import Services from '$lib/components/Services.svelte'
	import Teaching from '$lib/components/Teaching.svelte'
	import Projects from '../lib/components/Projects.svelte'
</script>

<main>
	<Container>
		<Hero />
		<Projects />
		<Teaching />
		<Services />
		<Contact />
	</Container>
</main>
