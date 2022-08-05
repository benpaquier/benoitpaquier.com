<script>
	import Section from './Section.svelte'
</script>

<Section>
	<h3>Contact</h3>
	<div class="grid">
		<div class="grid-item">
			<ul>
				<li>
					<p>• <a href="mailto:hello@benoitpaquier.com">hello@benoitpaquier.com</a></p>
				</li>
				<li>
					<p>
						• <a href="https://www.linkedin.com/in/benoit-paquier-8b485160/" target="_blank"
							>Linkedin</a
						>
					</p>
				</li>
				<li>
					<p>• <a href="https://github.com/benpaquier/" target="_blank">Github</a></p>
				</li>
			</ul>
		</div>
		<div class="grid-item">
			<picture>
				<source srcset="/images/contact/contact.webp" type="image/webp" />
				<source srcset="/images/contact/contact.jpeg" type="image/jpeg" />
				<img src="/images/contact/contact.jpeg" alt="Benoit Paquier" width="300" height="388" />
			</picture>
		</div>
	</div>
</Section>

<style>
	h3 {
		font-family: 'Raleway-Black', sans-serif;
		font-size: 3rem;
		margin-bottom: 2rem;
	}

	.grid {
		display: flex;
		width: 640px;
		margin: 0 auto;
	}

	.grid-item {
		display: flex;
		flex-direction: column;
		justify-content: center;
		width: 320px;
	}

	p {
		font-family: 'Raleway-Bold', sans-serif;
		margin-bottom: 2rem;
	}

	a {
		color: var(--teal);
	}

	img {
		width: 300px;
		filter: grayscale(0.8);
		transition: filter 2s;
		box-shadow: 20px 20px 0px 4px var(--darkBlue);
	}

	img:hover {
		filter: grayscale(0.4);
	}

	@media (max-width: 768px) {
		.grid {
			display: flex;
			width: 100%;
			flex-direction: column;
		}
	}
</style>
