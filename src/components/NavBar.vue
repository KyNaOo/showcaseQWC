<script setup>
import { ref } from "vue";
import { RouterLink } from "vue-router";

const isOpen = ref(false);

const toggleMenu = () => {
  isOpen.value = !isOpen.value;
};
</script>

<template>
  <header class="bg-white shadow-sm sticky top-0 z-50">
    <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between h-16">
        <div class="flex-shrink-0 flex items-center">
          <RouterLink to="/" class="text-xl font-bold text-gray-800">
            Logo
          </RouterLink>
        </div>

        <div class="hidden sm:flex sm:space-x-8 sm:items-center">
          <RouterLink
            to="/"
            class="text-gray-600 hover:text-gray-900 px-3 py-2 text-sm font-medium transition-colors duration-200"
            active-class="text-gray-900 font-semibold"
          >
            Home
          </RouterLink>

          <RouterLink
            to="/about"
            class="text-gray-600 hover:text-gray-900 px-3 py-2 text-sm font-medium transition-colors duration-200"
            active-class="text-gray-900 font-semibold"
          >
            About us
          </RouterLink>
        </div>

        <!-- Mobile hamburger -->
        <div class="flex items-center sm:hidden">
          <button
            @click="toggleMenu"
            class="inline-flex items-center justify-center p-2 rounded-md text-gray-600 hover:text-gray-900 hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-gray-500"
            :aria-expanded="isOpen"
          >
            <span class="sr-only">Open main menu</span>
            <svg
              v-if="!isOpen"
              class="block h-6 w-6"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M4 6h16M4 12h16M4 18h16"
              />
            </svg>
            <svg
              v-else
              class="block h-6 w-6"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M6 18L18 6M6 6l12 12"
              />
            </svg>
          </button>
        </div>
      </div>

      <!-- Mobile menu -->
      <div v-show="isOpen" class="sm:hidden">
        <div class="pt-2 pb-3 space-y-1">
          <RouterLink
            to="/"
            class="block px-3 py-2 text-base font-medium text-gray-600 hover:text-gray-900 hover:bg-gray-50 rounded-md transition-colors duration-200"
            active-class="bg-gray-50 text-gray-900 font-semibold"
            @click="isOpen = false"
          >
            Home
          </RouterLink>

          <RouterLink
            to="/about"
            class="block px-3 py-2 text-base font-medium text-gray-600 hover:text-gray-900 hover:bg-gray-50 rounded-md transition-colors duration-200"
            active-class="bg-gray-50 text-gray-900 font-semibold"
            @click="isOpen = false"
          >
            About
          </RouterLink>
        </div>
      </div>
    </nav>
  </header>
</template>
