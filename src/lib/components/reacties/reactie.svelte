<script>
	export let data;
	let showImage = true; // Stel in op 'false' als er geen externe afbeelding is
</script>

<section>
	<article>
		<!-- {#each reactions as reaction} -->
		<figure>
			<svg width="" height="" viewBox="0 0 30 30" fill="none" xmlns="http://www.w3.org/2000/svg">
				<path
					fill-rule="evenodd"
					clip-rule="evenodd"
					d="M9.25975 1.14181C11.0796 0.387987 13.0302 0 15 0C16.9698 0 18.9204 0.387987 20.7403 1.14181C22.5601 1.89563 24.2137 3.00052 25.6066 4.3934C26.9995 5.78628 28.1044 7.43986 28.8582 9.25975C29.612 11.0796 30 13.0302 30 15C30 16.9698 29.612 18.9204 28.8582 20.7403C28.1044 22.5601 26.9995 24.2137 25.6066 25.6066C25.3425 25.8707 25.069 26.1245 24.7867 26.3675C24.7454 26.407 24.7019 26.444 24.6565 26.4783C23.4826 27.4659 22.1622 28.2692 20.7403 28.8582C18.9204 29.612 16.9698 30 15 30C13.0302 30 11.0796 29.612 9.25975 28.8582C7.43986 28.1044 5.78628 26.9995 4.3934 25.6066C3.00052 24.2137 1.89563 22.5601 1.14181 20.7403C0.387986 18.9204 0 16.9698 0 15C0 13.0302 0.387986 11.0796 1.14181 9.25975C1.89563 7.43987 3.00052 5.78628 4.3934 4.3934C5.78628 3.00052 7.43987 1.89563 9.25975 1.14181ZM24.1727 22.737C23.7111 22.0689 23.1411 21.4759 22.4814 20.9846C21.1864 20.0202 19.6146 19.4996 18 19.5H12C10.3873 19.4996 8.81752 20.019 7.52336 20.9812C6.8617 21.4731 6.29012 22.0674 5.82743 22.7372C5.03276 21.7951 4.38664 20.7346 3.91345 19.5922C3.31039 18.1363 3 16.5759 3 15C3 13.4241 3.31039 11.8637 3.91345 10.4078C4.5165 8.95189 5.40041 7.62902 6.51472 6.51472C7.62902 5.40042 8.95189 4.5165 10.4078 3.91345C11.8637 3.31039 13.4241 3 15 3C16.5759 3 18.1363 3.31039 19.5922 3.91345C21.0481 4.5165 22.371 5.40042 23.4853 6.51472C24.5996 7.62902 25.4835 8.95189 26.0866 10.4078C26.6896 11.8637 27 13.4241 27 15C27 16.5759 26.6896 18.1363 26.0866 19.5922C25.6134 20.7345 24.9673 21.795 24.1727 22.737ZM15 6C13.4087 6 11.8826 6.63214 10.7574 7.75736C9.63214 8.88258 9 10.4087 9 12C9 13.5913 9.63214 15.1174 10.7574 16.2426C11.8826 17.3679 13.4087 18 15 18C16.5913 18 18.1174 17.3679 19.2426 16.2426C20.3679 15.1174 21 13.5913 21 12C21 10.4087 20.3679 8.88258 19.2426 7.75736C18.1174 6.63214 16.5913 6 15 6Z"
					fill="#0594C6"
				/>
			</svg>
		</figure>
		<blockquote>
			<h2>Kees Hoffman</h2>
			<time datetime="2023-09-27">27 september 2023</time>
			<p>Dit is een citaat of een stukje tekst dat je wilt benadrukken.</p>
		</blockquote>
		<!-- {/each} -->
	</article>
</section>

<style>
	section {
		padding: var(--unit-default);
	}

	article {
		width: 20rem;
		background-color: var(--color-secundary);
		display: grid;
		grid-template-columns: 2.5rem 1fr;
		grid-template-rows: 1fr;
		grid-column-gap: var(--unit-small);
		grid-row-gap: 0px;
		padding: var(--unit-small);
		position: relative;
	}

	article h2 {
		font-size: 1rem;
		color: var(--color-primary);
	}

	figure:first-child {
		height: fit-content;
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content: center;
		gap: var(--unit-small);
	}

	/* form {
        grid-row-start: 3;
    } */

	svg {
		width: 2rem;
		height: 2rem;
		aspect-ratio: 1/1;
	}

	time {
		grid-area: 2 / 2 / 3 / 3;
		color: #aaaaaa;
	}

	blockquote {
		font-family: 'Poppins';
		font-style: italic;
		margin: 0;
		grid-area: 0 / 1;
		padding: 0;
		padding-left: 0.5rem;
	}

	blockquote p {
		position: relative;
		padding-left: var(--unit-small);
	}

	blockquote p::before {
		content: '"';
		color: var(--color-blue);
		font-size: 2rem;
		top: -0.5rem;
		left: -0.25rem;
		position: absolute;
	}

	/* If the container is larger than 768px */
	@media (min-width: 768px) {
		article {
			width: 25rem;
			margin-left: 20%;
		}
	}
</style>
