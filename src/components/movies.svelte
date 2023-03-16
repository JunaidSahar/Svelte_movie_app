<script>
  import MovieCard from "./movie-card.svelte";
  import Navbar from "./navbar.svelte";

  export let movies;
</script>

<section class="w-full bg-[#0B1723]">
  <Navbar />

  <div
    class="container h-screen mx-auto py-12 px-8 overflow-scroll scrollbar-hide"
  >
    <h3 class="text-2xl text-white font-semibold mb-8">Most Popular</h3>
    <div class="grid grid-cols-6 gap-x-10 gap-y-20">
      {#each movies as movie}
        <MovieCard {movie} />
      {/each}
    </div>
  </div>
</section>

<style>
  .scrollbar-hide::-webkit-scrollbar {
    display: none;
  }

  /* For IE, Edge and Firefox */
  .scrollbar-hide {
    -ms-overflow-style: none; /* IE and Edge */
    scrollbar-width: none; /* Firefox */
  }
</style>
