<template>
  <section
    class="min-h-screen flex items-center justify-center bg-zinc-950 px-6 pt-24"
  >
    <div class="max-w-4xl text-center">
      <h1
        class="text-5xl md:text-6xl font-bold text-white mb-6 animate-fade-in-up"
      >
        Hi, I'm
        <span class="text-blue-500 relative">
          Anas Allahham
          <span
            class="absolute inset-0 bg-blue-500/20 blur-xl rounded-full"
          ></span>
        </span>
      </h1>

      <h2
        class="text-xl md:text-2xl text-zinc-400 mb-8 animate-fade-in-up"
        style="animation-delay: 0.1s"
      >
        Flutter & Frontend Developer building scalable apps and modern
        dashboards.
      </h2>

      <div
        class="flex justify-center gap-4 animate-fade-in-up"
        style="animation-delay: 0.2s"
      >
        <a
          href="#projects"
          class="px-6 py-3 bg-blue-500 text-white rounded-lg hover:bg-blue-600 hover:shadow-lg hover:shadow-blue-500/25 transition-all duration-300 transform hover:-translate-y-0.5"
        >
          View Projects
        </a>

        <a
          href="#contact"
          class="px-6 py-3 border border-zinc-700 text-zinc-300 rounded-lg hover:border-blue-500 hover:text-blue-500 hover:bg-zinc-800/50 transition-all duration-300"
        >
          Contact Me
        </a>
      </div>
    </div>
  </section>
</template>

<style scoped>
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.animate-fade-in-up {
  animation: fadeInUp 0.6s ease-out forwards;
  opacity: 0;
}
</style>
