<script>
  import { onMount } from "svelte";
  import Hero from "../components/hero.svelte";
  import Movies from "../components/movies.svelte";
  import Navbar from "../components/navbar.svelte";

  let movies = [];

  onMount(() => {
    fetch("https://api.tvmaze.com/shows")
      .then((response) => response.json())
      .then((result) => (movies = result));
  });
</script>

<section>
  <Navbar />
  <Hero />
  <Movies {movies} />
</section>
