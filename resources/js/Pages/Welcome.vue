<template>
  <div class="min-h-screen bg-black text-white relative overflow-hidden px-4 p-5">
    <!-- Particle Background -->
    <div id="particles-js" class="absolute inset-0 z-0"></div>

    <!-- Navigation -->
    <nav-link>  </nav-link>
    <!-- Hero Section -->
    <section class="flex flex-col items-center justify-center text-center pt-10 md:pt-20 z-10 relative">
      <h1 class="text-4xl sm:text-5xl md:text-6xl font-bold text-gold font-serif leading-tight max-w-4xl">
        The Magic of NFTs Awakens with Dlphic
      </h1>
      <p class="text-lg md:text-xl text-gray-300 mt-4 max-w-2xl">
        Explore a realm where Shaolin fruits and wizardry collide in mystical NFT enchantments.
      </p>
      <div class="mt-6 flex flex-col sm:flex-row gap-4">
        <a
            href="https://opensea.io/collection/shaolin-fruits-1"
            target="_blank"
            class="bg-gold text-black px-6 py-3 rounded-lg font-bold hover:scale-105 transition"
        >
          View Collection
        </a>
        <a
            href="https://x.com/YOUR_HANDLE"
            target="_blank"
            class="bg-white/10 border border-gold text-gold px-6 py-3 rounded-lg hover:bg-gold hover:text-black transition"
        >
          Follow on X
        </a>
      </div>
    </section>

    <!-- Showcase Section -->
    <section id="collection" class="mt-20 md:mt-32 z-10 relative text-center">
      <h2 class="text-3xl md:text-4xl font-bold text-gold mb-8 magic-glow">Meet the Magic</h2>
      <div class="max-w-4xl mx-auto">
        <img
            src="/images/dogAndOrange.webp"
            alt="Wizard NFTs"
            class="rounded-lg shadow-xl mx-auto w-full object-cover"
        />
      </div>
    </section>

    <!-- About Section -->
    <section id="about" class="mt-20 md:mt-32 z-10 relative text-center max-w-3xl mx-auto">
      <h2 class="text-3xl md:text-4xl font-bold text-gold mb-6">About Dlphic</h2>
      <p class="text-gray-300 text-lg">
        Dlphic is a mystical NFT experience where magical fruits, ancient wisdom, and crypto collide. Our mission is to enchant your digital wallet with rare, story-driven collectibles that awaken your inner wizard.
      </p>
    </section>

    <!-- Join / Subscribe Section -->
    <section id="join" class="mt-20 md:mt-32 mb-20 z-10 relative text-center max-w-xl mx-auto">
      <h2 class="text-2xl md:text-3xl font-bold text-gold mb-4">Join the Spell Circle</h2>
      <p class="text-gray-400 mb-4">Be first to know when the portal opens.</p>
      <form @submit.prevent class="flex flex-col sm:flex-row gap-4 justify-center">
        <input
            type="email"
            placeholder="Your email address"
            class="w-full sm:w-auto px-4 py-3 rounded-lg text-black"
            required
        />
        <button type="submit" class="bg-gold text-black px-6 py-3 rounded-lg font-bold hover:scale-105 transition">
          Join Waitlist
        </button>
      </form>
    </section>
  </div>
</template>

<script setup>
import { onMounted } from 'vue';
import NavLink from "@/Components/NavLink.vue";

onMounted(() => {
  const waitForParticlesJS = setInterval(() => {
    if (window.particlesJS) {
      clearInterval(waitForParticlesJS);
      window.particlesJS('particles-js', {
        particles: {
          number: { value: 50, density: { enable: true, value_area: 800 } },
          color: { value: '#d4af37' },
          shape: { type: 'circle' },
          opacity: { value: 0.6, random: true },
          size: { value: 3, random: true },
          move: { enable: true, speed: 1.5, out_mode: 'out' },
        },
        interactivity: {
          events: {
            onhover: { enable: true, mode: 'repulse' },
            onclick: { enable: true, mode: 'push' },
          },
          modes: {
            repulse: { distance: 100, duration: 0.4 },
            push: { particles_nb: 4 },
          },
        },
        retina_detect: true,
      });
    }
  }, 100);
});
</script>

<style scoped>
.text-gold {
  color: #d4af37;
}
.bg-gold {
  background-color: #d4af37;
}
#particles-js {
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;
  z-index: 0;
}
.magic-glow {
  color: #d4af37;
  text-shadow: 0 0 5px #d4af37, 0 0 10px #d4af37, 0 0 20px #fff;
  animation: glowPulse 2s ease-in-out infinite alternate;
}

@keyframes glowPulse {
  from {
    text-shadow: 0 0 5px #d4af37, 0 0 10px #d4af37, 0 0 20px #fff;
  }
  to {
    text-shadow: 0 0 10px rgba(255, 255, 255, 0.38), 0 0 20px #d4af37, 0 0 30px rgba(255, 255, 255, 0.61);
  }
}
</style>

<!-- Make sure particles.js is loaded in the Blade layout -->
<!-- <script src="https://cdn.jsdelivr.net/npm/particles.js@2.0.0/particles.min.js"></script> -->
