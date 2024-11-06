<script setup>
import { RouterView } from "vue-router";
import Footer from "./components/Footer.vue";
import NavBar from "./components/NavBar.vue";
</script>

<template>
  <div class="flex flex-col min-h-screen">
    <NavBar />
    <RouterView class="flex-grow" />
    <Footer />
  </div>
</template>

<style scoped></style>
