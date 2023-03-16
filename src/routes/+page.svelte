<script>
  import { onMount } from "svelte";
  import Hero from "../components/hero.svelte";
  import Movies from "../components/movies.svelte";
  import Navbar from "../components/navbar.svelte";
  import Sidenav from "../components/sidenav.svelte";

  let movies = [];

  onMount(() => {
    fetch("https://api.tvmaze.com/shows")
      .then((response) => response.json())
      .then((result) => (movies = result));
  });
</script>

<section>
  <div class="flex">
    <Sidenav />
    <Movies {movies} />
  </div>
</section>
