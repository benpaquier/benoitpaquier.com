<script>
	export let src, title, link

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
		<div class="img" style={`background-image: url(${src});`} />
		<p>{title}</p>
	</article>
</a>

<style>
	a {
		text-decoration: none;
	}

	article {
		position: relative;
		height: 368px;
		display: flex;
		align-items: flex-end;
		border-radius: 6px;
		box-shadow: 0px 0px 17px -10px rgba(0, 0, 0, 0.2);
		overflow: hidden;
		background-color: transparent;
		transition: all 0.3s ease-out 0s;
	}

	.img {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background-position: center;
		background-size: cover;
		background-repeat: no-repeat;
		transition: all 0.3s ease-out 0s;
	}

	article.active {
		background-color: black;
	}

	article.active .img {
		opacity: 0.75;
	}

	p {
		color: white;
		font-family: 'Raleway-Bold';
		z-index: 2;
		padding-left: 1rem;
		padding-bottom: 1rem;
		opacity: 0;
		transition: all 0.3s ease-out 0s;
	}

	article.active p {
		opacity: 1;
	}

	@media (max-width: 992px) {
		p {
			opacity: 1;
		}
	}
</style>
