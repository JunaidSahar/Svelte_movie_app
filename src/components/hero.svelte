<script>
  import "../app.css";
</script>

<section
  class="h-[750px] bg-no-repeat relative overflow-hidden w-full"
  style="background-size: cover; background-position: center;"
>
  <div class="backdrop-brightness-50 h-full w-full z-20">
    <div
      class="container mx-auto h-full flex flex-col justify-center items-start gap-2"
    >
      <h1 class="text-white text-7xl font-semibold mb-6">The Innocents</h1>
      <div class="flex gap-3 text-[#adb5bd] text-lg">
        <p>Drama</p>
        <p>Horror</p>
        <p>Mystery</p>
      </div>
      <div class="text-white flex items-center gap-4">
        <span class="font-semibold text-3xl">Episodes 8</span>
        <span
          class="text-[#45B8FF] cursor-pointer flex gap-2 py-1 px-8 rounded-lg border border-[#45B8FF] hover:bg-white hover:text-[#872DFE] hover:border-none transition-all duration-500"
        >
          <svg
            width="24"
            height="24"
            viewBox="0 0 24 24"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M11.969 2C6.44899 2 1.96899 6.48 1.96899 12C1.96899 17.52 6.44899 22 11.969 22C17.489 22 21.969 17.52 21.969 12C21.969 6.48 17.499 2 11.969 2ZM14.969 14.23L12.069 15.9C11.7199 16.1034 11.3231 16.2106 10.919 16.2106C10.5149 16.2106 10.1181 16.1034 9.76899 15.9C9.41711 15.6986 9.12515 15.4073 8.92305 15.0558C8.72096 14.7043 8.61602 14.3054 8.61899 13.9V10.55C8.61899 9.72 9.04899 8.97 9.76899 8.55C10.489 8.13 11.349 8.13 12.079 8.55L14.979 10.22C15.699 10.64 16.129 11.38 16.129 12.22C16.129 13.06 15.699 13.81 14.969 14.23Z"
              fill="#872DFE"
            />
          </svg>
          Play Now
        </span>
      </div>
    </div>
  </div>
  <video
    src="/vid9.mp4"
    autoplay
    loop
    muted
    playsinline
    id="myVideo"
    poster="https://sveltejs.github.io/assets/caminandes-llamigos.jpg"
    class="absolute top-0 -z-20 w-full h-full object-cover"
  >
    <track kind="captions" />
  </video>
</section>
