<script setup>
import { Head } from '@inertiajs/vue3'
import DlphicLogo from "@/Components/DlphicLogo.vue";
import NavLink from "@/Components/NavLink.vue";
</script>

<template>
  <Head title="Welcome to Dlphic" />
  <nav-link/>
  <div class="min-h-screen flex items-center justify-center bg-black text-white">
    <div class="text-center px-6 py-12 rounded-xl shadow-xl" style="background-color: #000000">
      <h1 class="text-4xl font-extrabold mb-4 text-green-500">Welcome to Dlphic</h1>
      <div class="logo flex justify-center">
        <dlphic-logo class="h-20 w-20 bg-white"/>
      </div>
      <p class="text-lg text-white p-3"><b>Page Coming Soon</b></p>
    </div>
  </div>
</template>

<style scoped>
.background {
  background-image: url('/images/dl_logo.png');
  background-repeat: no-repeat;
  background-size: cover; /* Ensures the image covers the container */
  background-position: center; /* Centers the image */
}
body {
  margin: 0;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
</style>