<script>
    export let wish
</script>

<img src={wish.image.url} width={wish.image.width} height={wish.image.height} alt="Afbeelding van {wish.heading}" />

<style>
    img {
        width: clamp(100%, 100%, 12rem); 
        background-color: var(--color-accent-100);  
        height: auto;
        aspect-ratio: 1/1;
        object-fit: cover;
        margin-bottom: var(--unit-small);
        display: block;
  max-width: 100%;
  max-height: 100%;
  /* dim unselected */
  opacity: 0.7;
  -webkit-transform: scale(0.85);
          transform: scale(0.85);
  -webkit-filter: blur(5px);
          filter: blur(5px);
  -webkit-transition: opacity 0.3s, -webkit-transform 0.3s, transform 0.3s, -webkit-filter 0.3s, filter 0.3s;
          transition: opacity 0.3s, transform 0.3s, filter 0.3s;
          border-radius: 5px;
    }


</style>