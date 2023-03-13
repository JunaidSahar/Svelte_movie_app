<script>
  export let movie;
</script>

<div>
  <div>
    <div class="h-96">
      <a href={movie.id}>
        <img
          class="h-full rounded-lg w-full object-cover"
          src={movie.image.medium}
          alt=""
        />
      </a>
    </div>
    <div class="py-3 flex flex-col">
      <span class="text-xl font-medium text-gray-700 truncate"
        >{movie.name}</span
      >
      <span class="text-[#5d5e5f]">{movie.language}</span>
    </div>
  </div>
</div>
