<script>
	export let src, alt, width, height, title, link

	let hoverClass = ''

	const onMouseEnter = () => {
		hoverClass = 'active'
	}

	const onMouseLeave = () => {
		hoverClass = ''
	}
</script>

<a href={link} target="_blank">
	<article class={hoverClass} on:mouseenter={onMouseEnter} on:mouseleave={onMouseLeave}>
		<img {alt} loading="lazy" decoding="async" {width} {height} {src} />
		<h5>{title}</h5>
	</article>
</a>

<style>
	a {
		text-decoration: none;
	}

	article {
		position: relative;
		width: 368px;
		height: 368px;
		display: flex;
		align-items: flex-end;
		border-radius: 6px;
		box-shadow: 0px 0px 17px -10px rgba(0, 0, 0, 0.2);
		overflow: hidden;
	}

	article img {
		position: absolute;
		width: 100%;
		height: 100%;
		transition: all 0.5s ease-out 0s;
	}

	article.active img {
		transform: scale(1.1);
	}

	h5 {
		color: white;
		font-family: 'Raleway-Bold';
		z-index: 2;
		padding-left: 1rem;
		padding-bottom: 1rem;
		opacity: 0;
		transition: all 0.5s ease-out 0s;
	}

	article.active h5 {
		opacity: 1;
	}
</style>
