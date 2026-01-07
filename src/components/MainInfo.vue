<template>
  <div class="h-screen w-full overflow-hidden">
    <div class="flex h-full">

      <div class="hidden md:block md:w-[50%] h-full">
        <div class="h-full bg-sky-100 flex items-center justify-center text-gray-500">
          <iframe
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d52893057.91949028!2d-161.59196462941878!3d35.98765464649458!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x54eab584e432360b%3A0x1c3bb99243deb742!2sUnited%20States!5e0!3m2!1sen!2sin!4v1767726315761!5m2!1sen!2sin"
            class="w-full h-full border-0" style="border:0;" allowfullscreen="" loading="lazy"
            referrerpolicy="no-referrer-when-downgrade"></iframe>
        </div>
      </div>

      <div class="w-full md:w-[50%] h-full overflow-y-auto bg-gray-50">
        <div class="p-4">
          <div class="mb-4">
            <h1 class="text-lg font-semibold">
              Austin, TX real estate & homes for sale
            </h1>
            <div class="flex justify-between text-sm text-gray-500 mt-1">
              <span>2,010 Homes</span>
              <div class="relative">
                <button @click="toggleDropdown('sell')" class=" flex items-center gap-1 cursor-pointer">
                  Sort By:
                  <select class="border-none outline-none text-sky-700 font-bold cursor-pointer">
                    <option selected value="New Listing">New Listing</option>
                    <option value="Most Viewed">Most Viewed</option>
                    <option value="Likes">Likes</option>
                  </select>
                </button>
              </div>
            </div>
          </div>

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


    <button class="fixed bottom-6 left-1/2 -translate-x-1/2 md:hidden
             bg-sky-700 text-white px-6 py-2 rounded-full shadow-lg flex items-center gap-2">
      Map
      <svg id='Map_20' width='20' height='20' viewBox='0 0 20 20' xmlns='http://www.w3.org/2000/svg'
        xmlns:xlink='http://www.w3.org/1999/xlink'>
        <g transform="matrix(0.32 0 0 0.32 10 10)">
          <path
            style="stroke: white; stroke-width: 2; stroke-dasharray: none; stroke-linecap: round; stroke-dashoffset: 0; stroke-linejoin: round; fill: none; fill-rule: nonzero; opacity: 1;"
            transform=" translate(-25, -25)"
            d="M 0.875 2 C 0.371094 2.0625 -0.00390625 2.492188 0 3 L 0 41 C -0.00390625 41.386719 0.214844 41.738281 0.5625 41.90625 L 12.5625 47.90625 C 12.839844 48.039063 13.160156 48.039063 13.4375 47.90625 L 25.03125 42.09375 L 37.59375 47.90625 C 37.875 48.03125 38.199219 48.019531 38.46875 47.875 L 49.46875 41.875 C 49.792969 41.703125 49.996094 41.367188 50 41 L 50 3 C 49.996094 2.652344 49.8125 2.328125 49.511719 2.148438 C 49.210938 1.96875 48.839844 1.960938 48.53125 2.125 L 37.96875 7.875 L 25.40625 2.09375 C 25.140625 1.96875 24.828125 1.96875 24.5625 2.09375 L 13 7.875 L 1.4375 2.09375 C 1.261719 2.007813 1.066406 1.976563 0.875 2 Z M 26 4.53125 L 37 9.625 L 37 45.4375 L 26 40.375 Z M 2 4.625 L 12 9.625 L 12 45.375 L 2 40.375 Z M 24 4.625 L 24 40.375 L 14 45.375 L 14 9.625 Z M 48 4.6875 L 48 40.40625 L 39 45.3125 L 39 9.59375 Z" />
        </g>
      </svg>

    </button>
  </div>
</template>

<script setup>
import ListingCard from './Card.vue'
</script>
