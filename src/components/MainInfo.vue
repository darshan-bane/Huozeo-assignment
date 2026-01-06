<template>
  <div class="h-screen w-full overflow-hidden">
    <div class="flex h-full">

      <!-- MAP (Desktop only) -->
      <div class="hidden md:block md:w-[50%] h-full">
        <div class="h-full bg-sky-100 flex items-center justify-center text-gray-500">
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d52893057.91949028!2d-161.59196462941878!3d35.98765464649458!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x54eab584e432360b%3A0x1c3bb99243deb742!2sUnited%20States!5e0!3m2!1sen!2sin!4v1767726315761!5m2!1sen!2sin"  class="w-full h-full border-0" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
        </div>
      </div>

      <!-- LISTINGS -->
      <div class="w-full md:w-[50%] h-full overflow-y-auto bg-gray-50">
        <div class="p-4">

          <!-- Header -->
          <div class="mb-4">
            <h1 class="text-lg font-semibold">
              Austin, TX real estate & homes for sale
            </h1>
            <div class="flex justify-between text-sm text-gray-500 mt-1">
              <span>2,010 Homes</span>
              <div class="flex items-center gap-1">
                <span class="text-sky-700 cursor-pointer">
                Sort by: New Listing 
              </span>
               <svg  id='Arrow_Button_Down_2_24' width='10' height='10' viewBox='0 0 24 24'
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
              </div>
            </div>
          </div>

          <!-- Cards -->
          <div class="space-y-4 lg:columns-2">
            <ListingCard />
            <ListingCard />
            <ListingCard />
            <ListingCard />
            <ListingCard />
            <ListingCard />
          </div>
        </div>
      </div>
    </div>

    <!-- Mobile Map Button -->
    <button
      class="fixed bottom-6 left-1/2 -translate-x-1/2 md:hidden
             bg-sky-700 text-white px-6 py-2 rounded-full shadow-lg flex items-center gap-2">
      Map
    </button>
  </div>
</template>

<script setup>
import ListingCard from './Card.vue'
</script>
