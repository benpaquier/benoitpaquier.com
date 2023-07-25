<script>
	import Section from '$lib/components/Section.svelte'
	import Project from '$lib/components/Project.svelte'

	// images
	import radiofrance from '$lib/assets/images/radiofrance.jpg?width=576&height=576&webp'
	import fairness from '$lib/assets/images/fairness.jpg?width=576&height=576&webp'
	import immby from '$lib/assets/images/immby.jpg?width=576&height=576&webp'
	import usewalter from '$lib/assets/images/usewalter.jpeg?width=576&height=576&webp'
	import vuse from '$lib/assets/images/vuse.png?width=576&height=576&webp'
	import volume7 from '$lib/assets/images/volume7.png?width=576&height=576&webp'
	import yapouni from '$lib/assets/images/yapouni.jpeg?width=576&height=576&webp'
	import yse from '$lib/assets/images/yse.jpeg?width=576&height=576&webp'
	import nink from '$lib/assets/images/nink.png?width=576&height=576&webp'
	import lyrebird from '$lib/assets/images/lyrebird.png?width=576&height=576&webp'
	import viensla from '$lib/assets/images/viens-la.png?width=576&height=576&webp'
	import koolicar from '$lib/assets/images/koolicare.png?width=576&height=576&webp'
	import ptp from '$lib/assets/images/paye-ta-pinte.png?width=576&height=576&webp'

	const width = 368
	const height = 368
</script>

<Section>
	<h3>Références</h3>
	<div class="grid">
		<Project src={radiofrance} title="Radiofrance" link="https://radiofrance.fr/" />
		<Project src={fairness} title="Fairness" link="https://fairness.coop/" />
		<Project src={immby} title="Immby" link="https://immby.com/" />
		<Project src={usewalter} title="Usewalter" link="https://usewalter.com/" />
		<Project src={vuse} title="Vuse.com" link="https://www.vuse.com/ca/en/" />
		<Project src={volume7} title="Volume7" link="https://volume7.io/" />
		<Project src={yapouni} title="Yapouni" link="https://yapouni.com/" />
		<Project src={yse} title="Ysé Paris" link="https://yse-paris.com/" />
		<Project src={nink} title="Nink" link="https://nink.netlify.app/" />
		<Project
			src={lyrebird}
			title="Lyrebird"
			link="https://www.descript.com/overdub?lyrebird=true"
		/>
		<Project src={viensla} title="Viens-la" link="https://viens-la.com/" />
		<Project src={koolicar} title="Koolicar" link="https://www.openfleet.com/" />
		<Project
			src={ptp}
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

	@media (max-width: 992px) {
		.grid {
			grid-template-columns: repeat(2, 1fr);
		}
	}

	@media (max-width: 576px) {
		.grid {
			grid-template-columns: repeat(1, 1fr);
		}
	}
</style>
