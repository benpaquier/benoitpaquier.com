<script>
	import Section from '$lib/components/Section.svelte'
	import Project from '$lib/components/Project.svelte'

	// images
	import usewalter from '$lib/assets/images/usewalter.jpeg?width=500&height=500&webp'
	import vuse from '$lib/assets/images/vuse.png?width=500&height=500&webp'
	import volume7 from '$lib/assets/images/volume7.png?width=500&height=500&webp'
	import yapouni from '$lib/assets/images/yapouni.jpeg?width=500&height=500&webp'
	import yse from '$lib/assets/images/yse.jpeg?width=500&height=500&webp'
	import nink from '$lib/assets/images/nink.png?width=500&height=500&webp'
	import lyrebird from '$lib/assets/images/lyrebird.png?width=500&height=500&webp'
	import viensla from '$lib/assets/images/viens-la.png?width=500&height=500&webp'
	import koolicar from '$lib/assets/images/koolicare.png?width=500&height=500&webp'
	import ptp from '$lib/assets/images/paye-ta-pinte.png?width=500&height=500&webp'

	const width = 368
	const height = 368
</script>

<Section>
	<h3>Références</h3>
	<div class="grid">
		<Project
			src={usewalter}
			{width}
			{height}
			alt="Usewalter"
			title="Usewalter"
			link="https://usewalter.com/"
		/>
		<Project
			src={vuse}
			{width}
			{height}
			alt="Vuse.com"
			title="Vuse.com"
			link="https://www.vuse.com/ca/en/"
		/>
		<Project
			src={volume7}
			{width}
			{height}
			alt="Volume7"
			title="Volume7"
			link="https://volume7.io/"
		/>
		<Project
			src={yapouni}
			{width}
			{height}
			alt="Yapouni"
			title="Yapouni"
			link="https://yapouni.com/"
		/>
		<Project
			src={yse}
			{width}
			{height}
			alt="Ysé Paris"
			title="Ysé Paris"
			link="https://yse-paris.com/"
		/>
		<Project src={nink} {width} {height} alt="Nink" title="Nink" link="https://nink.netlify.app/" />
		<Project
			src={lyrebird}
			{width}
			{height}
			alt="Lyrebird"
			title="Lyrebird"
			link="https://www.descript.com/overdub?lyrebird=true"
		/>
		<Project
			src={viensla}
			{width}
			{height}
			alt="Viens-la"
			title="Viens-la"
			link="https://viens-la.com/"
		/>
		<Project
			src={koolicar}
			{width}
			{height}
			alt="Koolicar"
			title="Koolicar"
			link="https://www.openfleet.com/"
		/>
		<Project
			src={ptp}
			{width}
			{height}
			alt="Paye ta pinte"
			title="Paye ta pinte"
			link="https://www.behance.net/gallery/28324731/Paye-Ta-Pinte-MOBILE-APP?fbclid=IwAR110DYxld2j7nK2ZA3WqM1dP7bcYNEv_5kEsKQ2sd-ebkrDxUKw_3_6Pxc"
		/>
	</div>
</Section>

<style>
	.grid {
		display: grid;
		grid-template-columns: repeat(3, 1fr);
		gap: 2rem;
	}
</style>
