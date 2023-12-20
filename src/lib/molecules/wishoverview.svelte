<script>
	import WishHeading from '$lib/atoms/wish-heading.svelte';
	import WishImage from '$lib/atoms/wish-image.svelte';

	export let wish;
</script>

<li class="carousel-cell">
	<WishImage {wish} />
	<div>
		<a href="wens/{wish.id}" class="hero glitch layers" data-text="{wish.heading}">
			<span>
				<WishHeading {wish} />
			</span>
			
		</a>
		<p>Geplaatst op: {wish.date}</p>
		<p>Supporters: <span>4</span></p>
	</div>
</li>

<style>
	/* Stefan overzichtspagina */
	li {
		padding: var(--unit-default);
		background-color: var(--color-secundary);
        list-style: none;
		width: 40%;
  		height: 400px;
		display: flex;
		flex-flow: column nowrap;
		-webkit-box-pack: center;
  -webkit-justify-content: center;
          justify-content: center;
  -webkit-align-items: center;
          align-items: center;
		  padding: 5em;
		  margin-left: 5px;
		  margin-right: 5px;
		  background: linear-gradient(to bottom, rgba(255,255,255,0.15) 0%, rgba(0,0,0,0.15) 100%), radial-gradient(at top center, rgba(255,255,255,0.40) 0%, rgba(0,0,0,0.40) 120%) #989898;
 background-blend-mode: multiply,multiply;
	}

	li p{
		color:white;
		display: none;
	}
	span{
		display: none;
	}
    .grid-overview li {
		width: 20rem;
    }

	li div {
		display: flex;
		flex-direction: column;
	}

	li a {
		width: fit-content;
		height: fit-content;
		color: var(--color-primary-50);
		padding: var(--unit-micro);
		transition: var(--animation-default) ease-in-out;
		border-radius: var(--unit-micro);
		margin-bottom: var(--unit-default);
	}

	li a:is(:hover, :focus) {
		color: var(--color-secundary-pure);
		background-color: var(--color-blue);
	}

	li img {
		width: 100%;
		height: 20rem;
		object-fit: cover;
		margin-bottom: var(--unit-default);
		background-color: var(--color-primary-50);
		border-radius: var(--unit-micro);

		
	}

	li h2 {
		display: -webkit-box;
		-webkit-line-clamp: 2;
		-webkit-box-orient: vertical;
		overflow: hidden;
		margin: var(--unit-default) 0 var(--unit-small);
	}

	time {
		display: flex;
		align-items: center;
		gap: var(--unit-small);
		margin-bottom: var(--unit-default);
	}

	/* li {
		background-color: var(--color-secundary);
		border: 2px solid var(--color-accent-75);
		border-radius: var(--unit-small);
        padding: var(--unit-small);
    } */

	/* Inhoud met wensen in lijstweergave */
	.list-overview ul li {
		display: grid;
		grid-template-columns: 1fr;
		align-items: center;
		gap: var(--unit-large);
		padding: var(--unit-small);
		margin-bottom: var(--unit-default);
		border-bottom: 2px solid var(--color-accent-75);
	}

	.list-overview article li {
		width: 100%;
        height: 20rem;
		display: grid;
		grid-template-columns: 1fr 1fr;
		grid-template-rows: 1fr;
		padding: var(--unit-default);
		border-radius: var(--unit-small);
		background-color: var(--color-secundary);
		animation: fade-in var(--animation-default) ease-in-out;
		height: 20rem;
	}

	/* Inhoud met wensen in rasterweergave */
	.grid-overview ul {
		display: grid;
		grid-template-columns: 1fr;
		gap: var(--unit-default);
	}

	.grid-overview ul li {
		padding: var(--unit-default);
		background-color: var(--color-secundary);
		border: 2px solid var(--color-accent-75);
		border-radius: var(--unit-small);
		padding: var(--unit-small);
        display: grid;
		grid-template-columns: 1fr;
		grid-template-rows: 20rem 1fr;
	}

	#custom-view {
		transition: var(--animation-default) ease-in-out;
	}



.hero {
  line-height: 1;
  display: inline-block;
  color: #fff;
  z-index: 2;
  letter-spacing: 10px;

  filter: drop-shadow(0 1px 3px);
}


.layers {
  position: relative;
}

.layers::before,
.layers::after {
  content: attr(data-text);
  position: absolute;
  width: 110%;
  z-index: -1;
  display: none;
}

.layers::before {
  top: 10px;
  left: 15px;
  color: #e0287d;
}

.layers::after {
  top: 5px;
  left: -10px;
  color: #1bc7fb;
}



.paths {
  animation: paths 5s step-end infinite;
}

@keyframes paths {
  0% {
    clip-path: polygon(
      0% 43%,
      83% 43%,
      83% 22%,
      23% 22%,
      23% 24%,
      91% 24%,
      91% 26%,
      18% 26%,
      18% 83%,
      29% 83%,
      29% 17%,
      41% 17%,
      41% 39%,
      18% 39%,
      18% 82%,
      54% 82%,
      54% 88%,
      19% 88%,
      19% 4%,
      39% 4%,
      39% 14%,
      76% 14%,
      76% 52%,
      23% 52%,
      23% 35%,
      19% 35%,
      19% 8%,
      36% 8%,
      36% 31%,
      73% 31%,
      73% 16%,
      1% 16%,
      1% 56%,
      50% 56%,
      50% 8%
    );
  }

  5% {
    clip-path: polygon(
      0% 29%,
      44% 29%,
      44% 83%,
      94% 83%,
      94% 56%,
      11% 56%,
      11% 64%,
      94% 64%,
      94% 70%,
      88% 70%,
      88% 32%,
      18% 32%,
      18% 96%,
      10% 96%,
      10% 62%,
      9% 62%,
      9% 84%,
      68% 84%,
      68% 50%,
      52% 50%,
      52% 55%,
      35% 55%,
      35% 87%,
      25% 87%,
      25% 39%,
      15% 39%,
      15% 88%,
      52% 88%
    );
  }

  30% {
    clip-path: polygon(
      0% 53%,
      93% 53%,
      93% 62%,
      68% 62%,
      68% 37%,
      97% 37%,
      97% 89%,
      13% 89%,
      13% 45%,
      51% 45%,
      51% 88%,
      17% 88%,
      17% 54%,
      81% 54%,
      81% 75%,
      79% 75%,
      79% 76%,
      38% 76%,
      38% 28%,
      61% 28%,
      61% 12%,
      55% 12%,
      55% 62%,
      68% 62%,
      68% 51%,
      0% 51%,
      0% 92%,
      63% 92%,
      63% 4%,
      65% 4%
    );
  }

  45% {
    clip-path: polygon(
      0% 33%,
      2% 33%,
      2% 69%,
      58% 69%,
      58% 94%,
      55% 94%,
      55% 25%,
      33% 25%,
      33% 85%,
      16% 85%,
      16% 19%,
      5% 19%,
      5% 20%,
      79% 20%,
      79% 96%,
      93% 96%,
      93% 50%,
      5% 50%,
      5% 74%,
      55% 74%,
      55% 57%,
      96% 57%,
      96% 59%,
      87% 59%,
      87% 65%,
      82% 65%,
      82% 39%,
      63% 39%,
      63% 92%,
      4% 92%,
      4% 36%,
      24% 36%,
      24% 70%,
      1% 70%,
      1% 43%,
      15% 43%,
      15% 28%,
      23% 28%,
      23% 71%,
      90% 71%,
      90% 86%,
      97% 86%,
      97% 1%,
      60% 1%,
      60% 67%,
      71% 67%,
      71% 91%,
      17% 91%,
      17% 14%,
      39% 14%,
      39% 30%,
      58% 30%,
      58% 11%,
      52% 11%,
      52% 83%,
      68% 83%
    );
  }

  76% {
    clip-path: polygon(
      0% 26%,
      15% 26%,
      15% 73%,
      72% 73%,
      72% 70%,
      77% 70%,
      77% 75%,
      8% 75%,
      8% 42%,
      4% 42%,
      4% 61%,
      17% 61%,
      17% 12%,
      26% 12%,
      26% 63%,
      73% 63%,
      73% 43%,
      90% 43%,
      90% 67%,
      50% 67%,
      50% 41%,
      42% 41%,
      42% 46%,
      50% 46%,
      50% 84%,
      96% 84%,
      96% 78%,
      49% 78%,
      49% 25%,
      63% 25%,
      63% 14%
    );
  }

  90% {
    clip-path: polygon(
      0% 41%,
      13% 41%,
      13% 6%,
      87% 6%,
      87% 93%,
      10% 93%,
      10% 13%,
      89% 13%,
      89% 6%,
      3% 6%,
      3% 8%,
      16% 8%,
      16% 79%,
      0% 79%,
      0% 99%,
      92% 99%,
      92% 90%,
      5% 90%,
      5% 60%,
      0% 60%,
      0% 48%,
      89% 48%,
      89% 13%,
      80% 13%,
      80% 43%,
      95% 43%,
      95% 19%,
      80% 19%,
      80% 85%,
      38% 85%,
      38% 62%
    );
  }

  1%,
  7%,
  33%,
  47%,
  78%,
  93% {
    clip-path: none;
  }
}

.movement {
  position: relative;
  animation: movement 8s step-end infinite;
}

@keyframes movement {
  0% {
    top: 0px;
    left: -20px;
  }

  15% {
    top: 10px;
    left: 10px;
  }

  60% {
    top: 5px;
    left: -10px;
  }

  75% {
    top: -5px;
    left: 20px;
  }

  100% {
    top: 10px;
    left: 5px;
  }
}

.opacity {
  animation: opacity 5s step-end infinite;
}

@keyframes opacity {
  0% {
    opacity: 0.1;
  }

  5% {
    opacity: 0.7;
  }

  30% {
    opacity: 0.4;
  }

  45% {
    opacity: 0.6;
  }

  76% {
    opacity: 0.4;
  }

  90% {
    opacity: 0.8;
  }

  1%,
  7%,
  33%,
  47%,
  78%,
  93% {
    opacity: 0;
  }
}

.font {
  animation: font 7s step-end infinite;
}

@keyframes font {
  0% {
    font-weight: 100;
    color: #e0287d;
    filter: blur(3px);
  }

  20% {
    font-weight: 500;
    color: #fff;
    filter: blur(0);
  }

  50% {
    font-weight: 300;
    color: #1bc7fb;
    filter: blur(2px);
  }

  60% {
    font-weight: 700;
    color: #fff;
    filter: blur(0);
  }

  90% {
    font-weight: 500;
    color: #e0287d;
    filter: blur(6px);
  }
}

.glitch span {
  animation: paths 5s step-end infinite;
}

.glitch::before {
  animation: paths 5s step-end infinite, opacity 5s step-end infinite,
    font 8s step-end infinite, movement 10s step-end infinite;
}

.glitch::after {
  animation: paths 5s step-end infinite, opacity 5s step-end infinite,
    font 7s step-end infinite, movement 8s step-end infinite;
}



	@media (min-width: 440px) {
		.grid-overview ul {
			grid-template-columns: 1fr 1fr;
		}
	}

	@media (min-width: 500px) {
		.list-overview ul li {
			grid-template-columns: 12rem 1fr;
		}
	}

	@media (min-width: 628px) {
		.grid-overview ul {
			grid-template-columns: 1fr 1fr 1fr;
		}
	}

	/* Zichtbaarheids instelling */
	.javascriptEnabledNav {
		display: flex;
	}
</style>
