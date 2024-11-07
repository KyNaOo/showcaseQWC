<script setup>
import { ref } from "vue";
import { RouterLink } from "vue-router";

const isOpen = ref(false);

const navItems = [
  { path: "/", label: "Home" },
  { path: "/about", label: "About me" },
  { path: "/certifications", label: "Certifications" },
  { path: "/contact", label: "Contact me" },
];

const toggleMenu = () => {
  isOpen.value = !isOpen.value;
};
</script>

<template>
  <header class="bg-[#CDBFBF] shadow-sm sticky top-0 z-50">
    <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between h-20">
        <div class="flex-shrink-0 flex items-center">
          <RouterLink to="/" class="text-xl font-bold text-gray-800">
            <img
              src="../logo-removebg-preview.png"
              class="h-20 w-auto object-contain"
            />
          </RouterLink>
        </div>

        <!-- Desktop navigation -->
        <div class="hidden sm:flex sm:space-x-8 sm:items-center">
          <RouterLink
            v-for="item in navItems"
            :key="item.path"
            :to="item.path"
            class="text-gray-700 px-4 py-2 text-base font-medium rounded-lg transition-all duration-500 font-lexend-exa hover:bg-white hover:shadow-md hover:scale-105"
            active-class="bg-white text-gray-900 font-semibold shadow-md"
          >
            {{ item.label }}
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
              :class="['block h-6 w-6', isOpen ? 'hidden' : 'block']"
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
              :class="['block h-6 w-6', !isOpen ? 'hidden' : 'block']"
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
            v-for="item in navItems"
            :key="item.path"
            :to="item.path"
            class="block px-3 py-2 text-base font-medium text-gray-600 hover:text-gray-900 hover:bg-gray-50 rounded-md transition-colors duration-700"
            active-class="bg-gray-50 text-gray-900 font-semibold"
            @click="isOpen = false"
          >
            {{ item.label }}
          </RouterLink>
        </div>
      </div>
    </nav>
  </header>
</template>
