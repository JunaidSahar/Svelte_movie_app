<script>
  import MovieCard from "./movie-card.svelte";

  export let movies;
</script>

<section>
  <div class="container mx-auto py-10">
    <h3 class="text-2xl font-semibold mb-8">Most Popular</h3>
    <div class="grid grid-cols-5 gap-10">
      {#each movies as movie}
        <MovieCard {movie} />
      {/each}
    </div>
  </div>
</section>
