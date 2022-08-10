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
	<article
		class={hoverClass}
		on:mouseenter={onMouseEnter}
		on:mouseleave={onMouseLeave}
		style={`background-image: url(${src});`}
	>
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
		background-position: center;
		background-size: 100%;
		background-repeat: no-repeat;
		transition: all 1s ease-out 0s;
	}

	article.active {
		background-size: 105%;
	}

	p {
		color: white;
		font-family: 'Raleway-Bold';
		z-index: 2;
		padding-left: 1rem;
		padding-bottom: 1rem;
		opacity: 0;
		transition: all 0.5s ease-out 0s;
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
