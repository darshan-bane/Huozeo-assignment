<template>
  <nav class="bg-slate-900 text-white">
    <div class="max-w-7xl mx-auto px-4">
      <div class="flex h-16 items-center justify-between">

        <!-- Logo -->
        <div class="text-xl font-bold">
          VueApp
        </div>

        <!-- Desktop Menu -->
        <div class="hidden md:flex gap-6">
          <a href="#" class="hover:text-emerald-400">Home</a>
          <a href="#" class="hover:text-emerald-400">About</a>
          <a href="#" class="hover:text-emerald-400">Services</a>
          <a href="#" class="hover:text-emerald-400">Contact</a>
        </div>

        <!-- Mobile Button -->
        <button
          @click="toggleMenu"
          class="md:hidden focus:outline-none"
        >
          <svg
            v-if="!isOpen"
            xmlns="http://www.w3.org/2000/svg"
            class="h-6 w-6"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
              d="M4 6h16M4 12h16M4 18h16" />
          </svg>

          <svg
            v-else
            xmlns="http://www.w3.org/2000/svg"
            class="h-6 w-6"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
              d="M6 18L18 6M6 6l12 12" />
          </svg>
        </button>

      </div>
    </div>

    <!-- Mobile Menu -->
    <div v-show="isOpen" class="md:hidden bg-slate-800 px-4 pb-4">
      <a class="block py-2 hover:text-emerald-400" href="#">Home</a>
      <a class="block py-2 hover:text-emerald-400" href="#">About</a>
      <a class="block py-2 hover:text-emerald-400" href="#">Services</a>
      <a class="block py-2 hover:text-emerald-400" href="#">Contact</a>
    </div>
  </nav>
</template>

<script setup>
import { ref } from 'vue'

const isOpen = ref(false)
const toggleMenu = () => {
  isOpen.value = !isOpen.value
}
</script>
