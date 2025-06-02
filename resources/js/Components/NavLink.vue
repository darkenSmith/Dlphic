<template>
  <nav class="fixed top-0 w-full z-50 bg-black text-white shadow-md px-6 py-4 border-b border-white">
    <div class="flex justify-between items-center w-full">
      <!-- Logo -->
      <Link href="/" class="flex items-center space-x-2">
        <img src="/images/dl_logo.png" alt="Dlphic Logo" class="h-60 w-auto max-h-[100px]" />
      </Link>

      <!-- Hamburger Menu (Mobile Only) -->
      <button @click="toggleMenu" class="md:hidden text-white focus:outline-none">
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                d="M4 6h16M4 12h16M4 18h16" />
        </svg>
      </button>

      <!-- Desktop Nav Links (Right Aligned) -->
      <div class="hidden md:flex space-x-6">
        <Link :href="'/'" :class="linkClasses">Home</Link>
        <Link :href="'/Wizards'" :class="linkClasses">Wizards</Link>
        <Link :href="'/Music'" :class="linkClasses">Music</Link>
        <Link :href="'/Art'" :class="linkClasses">Art</Link>
        <Link :href="'/Community'" :class="linkClasses">Community</Link>
        <Link :href="'/NFT Projects'" :class="linkClasses">NFT Projects</Link>
      </div>
    </div>

    <!-- Mobile Nav Links (Stacked Below Logo) -->
    <div
        v-if="isMenuOpen"
        class="flex flex-col space-y-3 mt-4 md:hidden"
    >
      <Link :href="'/'" :class="linkClasses">Home</Link>
      <Link :href="'/Wizards'" :class="linkClasses">Wizards</Link>
      <Link :href="'/Music'" :class="linkClasses">Music</Link>
      <Link :href="'/Art'" :class="linkClasses">Art</Link>
      <Link :href="'/Community'" :class="linkClasses">Community</Link>
      <Link :href="'/NFT Projects'" :class="linkClasses">NFT Projects</Link>
    </div>
  </nav>
</template>

<script setup>
import {ref} from 'vue';
import {Link} from '@inertiajs/vue3';

const isMenuOpen = ref(false);
const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};

const linkClasses = 'block text-white hover:text-green-400 transition duration-200 font-bold';
</script>

<style scoped>
/* Tailwind handles layout – minimal scoped styling needed */
</style>