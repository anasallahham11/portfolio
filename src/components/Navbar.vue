<template>
  <header
    class="fixed top-0 left-0 w-full z-50 backdrop-blur-lg bg-zinc-950/80 border-b border-zinc-800/50"
  >
    <div class="container-custom h-16 flex items-center justify-between">
      <!-- Logo -->
      <div class="text-white font-semibold text-lg tracking-tight group">
        <span class="group-hover:text-blue-400 transition-colors duration-300"
          >Anas</span
        ><span class="text-blue-500">.</span>
      </div>

      <!-- Desktop Nav -->
      <nav class="hidden md:flex items-center gap-8 text-sm">
        <a
          v-for="link in navLinks"
          :key="link.href"
          :href="link.href"
          class="nav-link relative text-zinc-400 hover:text-white transition-colors duration-300"
        >
          {{ link.label }}
        </a>
      </nav>

      <!-- Desktop CTA -->
      <a
        href="#contact"
        class="hidden md:inline-block px-5 py-2 text-sm bg-blue-500 text-white rounded-lg hover:bg-blue-600 hover:shadow-lg hover:shadow-blue-500/25 transition-all duration-300"
      >
        Let's Talk
      </a>

      <!-- Mobile Menu Button -->
      <button
        @click="isMobileMenuOpen = !isMobileMenuOpen"
        class="md:hidden p-2 text-zinc-400 hover:text-white transition-colors"
        aria-label="Toggle menu"
      >
        <svg
          v-if="!isMobileMenuOpen"
          class="w-6 h-6"
          fill="none"
          stroke="currentColor"
          viewBox="0 0 24 24"
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
          class="w-6 h-6"
          fill="none"
          stroke="currentColor"
          viewBox="0 0 24 24"
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

    <!-- Mobile Menu -->
    <div
      v-if="isMobileMenuOpen"
      class="md:hidden bg-zinc-950/95 backdrop-blur-lg border-b border-zinc-800"
    >
      <nav class="container-custom py-4 flex flex-col gap-4 text-sm">
        <a
          v-for="link in navLinks"
          :key="link.href"
          :href="link.href"
          @click="isMobileMenuOpen = false"
          class="text-zinc-400 hover:text-white transition-colors duration-300 py-2"
        >
          {{ link.label }}
        </a>
        <a
          href="#contact"
          @click="isMobileMenuOpen = false"
          class="px-5 py-2 text-sm bg-blue-500 text-white rounded-lg hover:bg-blue-600 transition-all duration-300 text-center"
        >
          Let's Talk
        </a>
      </nav>
    </div>
  </header>
</template>

<script setup lang="ts">
import { ref } from "vue";

const navLinks = [
  { href: "#about", label: "About" },
  { href: "#skills", label: "Skills" },
  { href: "#projects", label: "Projects" },
  { href: "#contact", label: "Contact" },
];

const isMobileMenuOpen = ref(false);
</script>

<style scoped>
.nav-link::after {
  content: "";
  position: absolute;
  bottom: -4px;
  left: 0;
  width: 0;
  height: 2px;
  background: linear-gradient(90deg, #3b82f6, #60a5fa);
  transition: width 0.3s ease;
}

.nav-link:hover::after {
  width: 100%;
}
</style>
