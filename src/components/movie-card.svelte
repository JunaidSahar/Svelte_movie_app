<script>
  export let movie;
</script>

<div>
  <div>
    <div class="h-80">
      <a href={movie.id}>
        <img
          class="h-full w-full object-cover"
          src={movie.image.medium}
          alt=""
        />
      </a>
    </div>
    <div class="py-3 flex flex-col">
      <span class="text-xl font-normal text-white truncate">{movie.name}</span>
      <!-- <span class="text-[#5d5e5f]">{movie.language}</span> -->
    </div>
  </div>
</div>
