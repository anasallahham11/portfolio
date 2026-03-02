<template>
  <header
    class="fixed top-0 left-0 w-full z-50 backdrop-blur-xl bg-zinc-950/80 border-b border-zinc-800/50"
  >
    <div class="container-custom h-16 flex items-center justify-between">
      <!-- Logo with Avatar -->
      <a href="#" class="flex items-center gap-3 group">
        <div
          class="w-9 h-9 rounded-full overflow-hidden border-2 border-zinc-700 group-hover:border-blue-500 transition-colors shrink-0"
        >
          <img
            src="/profile.jpg"
            alt="Anas Allahham"
            class="w-full h-full object-cover"
          />
        </div>
        <span
          class="text-white font-bold text-xl tracking-tight whitespace-nowrap group-hover:text-blue-400 transition-colors duration-300"
          >Anas<span class="text-blue-500">.</span></span
        >
      </a>

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
        class="hidden md:inline-flex items-center gap-2 px-5 py-2.5 text-sm bg-blue-500 text-white rounded-xl hover:bg-blue-600 hover:shadow-lg hover:shadow-blue-500/25 transition-all duration-300"
      >
        Let's Talk
        <svg
          class="w-4 h-4"
          fill="none"
          stroke="currentColor"
          viewBox="0 0 24 24"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M17 8l4 4m0 0l-4 4m4-4H3"
          />
        </svg>
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
      class="md:hidden bg-zinc-950/95 backdrop-blur-xl border-b border-zinc-800"
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
          class="inline-flex items-center justify-center gap-2 px-5 py-2.5 text-sm bg-blue-500 text-white rounded-xl hover:bg-blue-600 transition-all duration-300"
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
