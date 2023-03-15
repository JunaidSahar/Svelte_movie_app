<script>
  import { onMount } from "svelte";
  import { page } from "$app/stores";
  import Navbar from "../../components/navbar.svelte";
  import "../../app.css";
  import { each } from "svelte/internal";

  let movie = [];

  const url = $page.url.pathname;

  onMount(() => {
    fetch("https://api.tvmaze.com/shows" + url)
      .then((response) => response.json())
      .then((result) => (movie = result));
  });

  console.log(movie);
</script>

<section>
  <Navbar />
  <div>
    <div
      class="bg-cover bg-center"
      style="background-image: url('{movie?.image?.original}');"
    >
      <div
        class="backdrop-brightness-50 py-16 h-full w-full backdrop-blur-sm backdrop-contrast-125"
      >
        <div
          class="container mx-auto h-full flex justify-between items-center space-y-4"
        >
          <div class="space-y-2">
            <h1 class="text-9xl text-white font-semibold">{movie?.name}</h1>
            <div class="flex gap-3 text-[#adb5bd] text-lg">
              <p>{movie?.premiered}</p>
              <span class="text-[#46B8FF]">|</span>
              <p>{movie?.genres}</p>
            </div>
            <div class="flex items-center text-white gap-3">
              <img src="rating.svg" class="w-28" alt="" />
              <span class="text-lg">{movie?.rating?.average}</span>
            </div>
            <h4 class="text-white">{movie.language}</h4>
          </div>
          <div>
            <img src={movie?.image?.medium} class="h-96" alt="" />
          </div>
        </div>
        <div class="container mx-auto h-full w-full">
          <h4 class="text-3xl text-white">Overview Of Series</h4>
          <p class="text-lg text-white">{@html movie?.summary}</p>
        </div>
      </div>
    </div>
  </div>
</section>
