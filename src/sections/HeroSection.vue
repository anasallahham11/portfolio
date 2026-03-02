<template>
  <section
    class="min-h-screen flex items-center justify-center bg-zinc-950 px-6 pt-24 relative overflow-hidden"
  >
    <!-- Animated background elements -->
    <div class="absolute inset-0 overflow-hidden">
      <!-- Floating orbs -->
      <div
        class="absolute top-1/4 -left-20 w-72 h-72 bg-blue-500/20 rounded-full blur-3xl animate-pulse"
      ></div>
      <div
        class="absolute bottom-1/4 -right-20 w-96 h-96 bg-blue-600/10 rounded-full blur-3xl animate-pulse"
        style="animation-delay: 1s"
      ></div>
      <div
        class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-150 h-150 bg-blue-500/5 rounded-full blur-3xl"
      ></div>

      <!-- Grid pattern overlay -->
      <div
        class="absolute inset-0 bg-[linear-gradient(rgba(255,255,255,0.02)_1px,transparent_1px),linear-gradient(90deg,rgba(255,255,255,0.02)_1px,transparent_1px)] bg-size-[60px_60px]"
      ></div>
    </div>

    <div class="max-w-4xl text-center relative z-10">
      <!-- Animated badge -->
      <div
        class="inline-flex items-center gap-2 px-4 py-2 bg-zinc-900/80 border border-zinc-800 rounded-full mb-8 animate-fade-in-up"
      >
        <span class="w-2 h-2 bg-green-500 rounded-full animate-pulse"></span>
        <span class="text-zinc-400 text-sm">Available for work</span>
      </div>

      <h1
        class="text-5xl md:text-7xl font-bold text-white mb-6 animate-fade-in-up"
        style="animation-delay: 0.1s"
      >
        Hi, I'm
        <span class="text-blue-500 relative inline-block"> Anas Allahham </span>
      </h1>

      <h2
        class="text-xl md:text-2xl text-zinc-400 mb-8 max-w-2xl mx-auto animate-fade-in-up"
        style="animation-delay: 0.2s"
      >
        <span class="text-white font-medium">Mobile & Frontend Developer</span>
        building scalable apps and modern dashboards that deliver exceptional
        user experiences.
      </h2>

      <div
        class="flex justify-center gap-4 animate-fade-in-up flex-wrap"
        style="animation-delay: 0.3s"
      >
        <a
          href="#projects"
          class="group px-8 py-3.5 bg-blue-500 text-white rounded-xl hover:bg-blue-600 hover:shadow-xl hover:shadow-blue-500/25 transition-all duration-300 transform hover:-translate-y-1"
        >
          <span class="flex items-center gap-2">
            View Projects
            <svg
              class="w-4 h-4 group-hover:translate-x-1 transition-transform"
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
          </span>
        </a>

        <a
          href="/Anas-Allahham.pdf"
          download
          class="group px-8 py-3.5 border border-zinc-700 text-zinc-300 rounded-xl hover:border-blue-500 hover:text-blue-500 hover:bg-zinc-800/50 transition-all duration-300 flex items-center gap-2"
        >
          <svg
            class="w-5 h-5"
            fill="none"
            stroke="currentColor"
            viewBox="0 0 24 24"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M12 10v6m0 0l-3-3m3 3l3-3m2 8H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z"
            />
          </svg>
          Download CV
        </a>

        <a
          href="#contact"
          class="group px-8 py-3.5 border border-zinc-700 text-zinc-300 rounded-xl hover:border-blue-500 hover:text-blue-500 hover:bg-zinc-800/50 transition-all duration-300 flex items-center gap-2"
        >
          <svg
            class="w-5 h-5"
            fill="none"
            stroke="currentColor"
            viewBox="0 0 24 24"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"
            />
          </svg>
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
