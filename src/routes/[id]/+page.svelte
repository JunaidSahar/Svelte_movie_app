<script>
  import { onMount } from "svelte";
  import { page } from "$app/stores";
  import Navbar from "../../components/navbar.svelte";
  import "../../app.css";

  let movie = [];

  const url = $page.url.pathname;

  onMount(() => {
    fetch("https://api.tvmaze.com/shows" + url)
      .then((response) => response.json())
      .then((result) => (movie = result));
  });

  console.log(movie.name);
</script>

<section>
  <Navbar />
  <div>
    {#if movie.length > 0}
      <div>
        <img src={movie.image.medium} alt={movie.name} />
        <span>{movie.name}</span>
      </div>
    {:else}
      asdasdas
    {/if}
  </div>
</section>
