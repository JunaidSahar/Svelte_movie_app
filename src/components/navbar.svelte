<nav class="bg-transparent relative">
  <div class="container px-6 py-8 mx-auto">
    <div class="lg:flex lg:items-center lg:justify-between">
      <div class="flex items-center justify-between">
        <div class="flex gap-5">
          <img src="/chevron-left.svg" alt="" />
          <img src="/chevron-right.svg" alt="" />
        </div>

        <!-- Mobile menu button -->
        <div class="flex lg:hidden">
          <button
            type="button"
            class="text-gray-500 dark:text-gray-200 hover:text-gray-600 dark:hover:text-gray-400 focus:outline-none focus:text-gray-600 dark:focus:text-gray-400"
            aria-label="toggle menu"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="w-6 h-6"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
              stroke-width="2"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M4 8h16M4 16h16"
              />
            </svg>

            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="w-6 h-6"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
              stroke-width="2"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M6 18L18 6M6 6l12 12"
              />
            </svg>
          </button>
        </div>
      </div>

      <!-- Mobile Menu open: "block", Menu closed: "hidden" -->
      <div
        class="absolute inset-x-0 z-20 w-full px-6 py-4 transition-all duration-300 ease-in-out bg-white dark:bg-gray-800 lg:mt-0 lg:p-0 lg:top-0 lg:relative lg:bg-transparent lg:w-auto lg:opacity-100 lg:translate-x-0 lg:flex lg:items-center"
      >
        <div class="flex items-center mt-4 gap-6 lg:mt-0">
          <img src="/search.svg" alt="" />
          <img src="/bell-notification.svg" alt="" />
          <div class="flex gap-2">
            <img src="/avatar.png" alt="" />
            <div class="text-white">
              <p class="-mb-2">Junaid Khan</p>
              <span class="text-[10px]">manage account</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</nav>
