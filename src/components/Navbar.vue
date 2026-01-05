<template>
  <header class="w-full border-b border-gray-200">

    <div class="hidden md:flex items-center justify-between px-6 py-4 w-full">
      <!-- Left: Logo -->
      <div class="flex items-center gap-2">
        <img src="/src/assets/images/navbar/houzeo_logo.png" alt="Houzeo" class="h-8" />
      </div>

      <!-- Center: Navigation -->
      <nav class="flex items-center flex-wrap justify-center gap-6 text-sm font-medium text-gray-700">
        <div class="relative">
          <button @click="toogleDropdown" class="hover:text-sky-700 flex items-center gap-1 cursor-pointer">Product
            <svg v-if="isOpen" id='Arrow_Button_Up_2_24' width='12' height='12' viewBox='0 0 24 24'
              xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'>
              <rect width='24' height='24' stroke='none' fill='#000000' opacity='0' />


              <g transform="matrix(0.85 0 0 0.85 12 12)">
                <path
                  style="stroke: none; stroke-width: 1; stroke-dasharray: none; stroke-linecap: butt; stroke-dashoffset: 0; stroke-linejoin: miter; stroke-miterlimit: 4; fill: rgb(0,0,0); fill-rule: nonzero; opacity: 1;"
                  transform=" translate(-12, -11.98)"
                  d="M 23.44 19 L 13.71 2.93 C 13.347434336968563 2.332281320588825 12.699086174749914 1.9672559954032565 12 1.9672559954032565 C 11.300913825250088 1.9672559954032565 10.652565663031439 2.332281320588825 10.290000000000001 2.9300000000000006 L 0.56 19 C 0.20464162785248918 19.61539963287007 0.20251993380241146 20.373146907100352 0.554426520307352 20.99052688342481 C 0.9063331068122924 21.607906859749267 1.5594120171268293 21.992189789491718 2.2700000000000005 22 L 21.73 22 C 22.440587982873172 21.992189789491718 23.09366689318771 21.607906859749267 23.445573479692648 20.99052688342481 C 23.79748006619759 20.373146907100352 23.79535837214751 19.61539963287007 23.44 19 Z"
                  stroke-linecap="round" />
              </g>
            </svg>
            <svg v-else id='Arrow_Button_Down_2_24' width='12' height='12' viewBox='0 0 24 24'
              xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'>
              <rect width='24' height='24' stroke='none' fill='#000000' opacity='0' />
              <g transform="matrix(0.85 0 0 0.85 12 12)">
                <path
                  style="stroke: none; stroke-width: 1; stroke-dasharray: none; stroke-linecap: butt; stroke-dashoffset: 0; stroke-linejoin: miter; stroke-miterlimit: 4; fill: rgb(0,0,0); fill-rule: nonzero; opacity: 1;"
                  transform=" translate(-12.01, -12.02)"
                  d="M 23.47 3 C 23.111318068259006 2.378731614548986 22.44736951687545 1.997151987317056 21.73 2 L 2.27 2 C 1.5594120171268289 2.007810210508281 0.906333106812292 2.3920931402507337 0.5544265203073517 3.0094731165751902 C 0.2025199338024115 3.626853092899647 0.20464162785248918 4.38460036712993 0.56 5 L 10.290000000000001 21.07 C 10.652565663031439 21.667718679411177 11.300913825250088 22.032744004596744 12 22.032744004596744 C 12.699086174749914 22.032744004596744 13.347434336968563 21.667718679411177 13.71 21.07 L 23.44 5 C 23.806593844495936 4.386569962478906 23.818030152970874 3.6241493974830945 23.47 2.9999999999999996 Z"
                  stroke-linecap="round" />
              </g>
            </svg>
          </button>
          <div v-show="isOpen" class="absolute top-8 transition z-10 flex flex-col gap-1 bg-white w-25 px-2 py-1 shadow-lg rounded-sm">
            <p> Product 1</p>
            <p> Product 2</p>
            <p> Product 3</p>
          </div>
        </div>

        <a href="#" class="hover:text-sky-700"">How Houzeo Works</a>
        <a href=" #" class="hover:text-sky-700"">Reviews</a>
        <a href=" #" class="hover:text-sky-700"">Buy</a>
        <a href=" #" class="hover:text-sky-700"">Sell</a>
        <a href=" #" class="hover:text-sky-700"">Pricing</a>
        <a href=" #" class="hover:text-sky-700"">Resources</a>
                <a href=" #" class="text-gray-600 hover:text-sky-700"">Sign In</a>

        <div class=" text-gray-600 text-xs">
          <div class="font-semibold">(844) 448-0110</div>
          <div class="text-gray-400">(9am to 6pm CST, Mon-Sat)</div>
    </div>
    </nav>

    <!-- Right: Actions -->
    <div class="flex items-center gap-4 text-sm">
      <button class=" bg-gradient-to-r from-sky-700 to-sky-800
    hover:from-sky-600 hover:to-sky-700 text-white px-4 py-2 rounded-md transition cursor-pointer">
        Start Free Listing
      </button>
    </div>
    </div>

    <!-- Mobile Header -->
    <div class="flex md:hidden items-center justify-between px-4 py-3">
      <!-- Hamburger -->
      <button class="p-2">
        <svg class="w-6 h-6 text-gray-700" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16" />
        </svg>
      </button>

      <!-- Logo -->
      <img src="/src/assets/images/navbar/houzeo_logo.png" alt="Houzeo" class="h-7" />

      <!-- Profile Icon -->
      <button class="p-2">
        <svg class="w-6 h-6 text-gray-700" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round"
            d="M5.121 17.804A9 9 0 1118.88 6.196M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
        </svg>
      </button>
    </div>
  </header>
</template>

<script setup>
import { ref } from 'vue';

const isOpen = ref(false)
const toogleDropdown = () => {
  isOpen.value = !isOpen.value
}
</script>
