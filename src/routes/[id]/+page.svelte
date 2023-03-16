<script>
  import { onMount } from "svelte";
  import { page } from "$app/stores";
  import Navbar from "../../components/navbar.svelte";
  import "../../app.css";
  import { each, HtmlTag } from "svelte/internal";
  import Sidenav from "../../components/sidenav.svelte";
  import Movies from "../../components/movies.svelte";

  let movie = [];
  let cast = [];

  const url = $page.url.pathname;

  onMount(() => {
    fetch("https://api.tvmaze.com/shows" + url)
      .then((response) => response.json())
      .then((result) => (movie = result));
  });

  onMount(() => {
    fetch("https://api.tvmaze.com/shows" + url + "?embed=cast")
      .then((response) => response.json())
      .then((result) => (cast = result._embedded.cast));
  });

  console.log(cast);
</script>

<section>
  <div class="flex">
    <Sidenav />
    <div class="w-full relative">
      <Navbar />
      <div
        class="h-screen absolute top-0 w-full"
        style="background-image: url({movie?.image
          ?.original}); background: #0B1723;
        background-blend-mode: multiply; background-position:center; background-size:cover; background-repeat:no-repeat;"
      >
        <div class="backdrop-blur-md h-full flex items-center">
          <div class="max-w-5xl px-20 space-y-5">
            <h1 class="text-7xl text-white">{movie.name}</h1>
            <div class="flex gap-3 text-white items-center">
              <img src="/rating.svg" alt="" /> |
              <span class="text-3xl text-white">{movie.rating?.average}</span>
            </div>
            <div class="flex gap-3 text-[#56FF71] items-center">
              <span class="text-lg text-white">{movie.premiered}</span> |
              <span class="text-lg text-white">{movie.genres}</span> |
              <span class="text-lg text-white">{movie.language}</span>
            </div>
            <p class="text-white font-light">{@html movie.summary}</p>
            <div class="flex gap-6">
              <a
                href=""
                class="flex text-white gap-2 px-12 py-2 border rounded-md"
                >Continue Play
                <img src="/play.svg" alt="" />
              </a>
              <a
                href=""
                class="flex text-white gap-2 px-12 py-2 border rounded-md"
                >Watch Later
                <img src="/later.svg" alt="" />
              </a>
            </div>
            <div class="">
              <h4 class="text-3xl text-white">Cast</h4>
              <div class="grid grid-cols-4 gap-8 mt-8">
                {#each cast as person}
                  <div class="flex gap-2 items-center w-full">
                    <img
                      src={person.person.image?.medium}
                      class="w-8 h-8 rounded-full object-cover"
                      alt=""
                    />
                    <p class="text-white">{person.person.name}</p>
                  </div>
                {/each}
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>
