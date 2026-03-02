<template>
  <section id="about" class="section-padding bg-zinc-950 relative">
    <!-- Background accents -->
    <div
      class="absolute top-0 right-0 w-1/3 h-full bg-linear-to-l from-blue-500/5 to-transparent"
    ></div>
    <div
      class="absolute bottom-0 left-0 w-1/3 h-full bg-linear-to-r from-blue-500/5 to-transparent"
    ></div>

    <div class="container-custom">
      <div class="grid md:grid-cols-2 gap-16 items-center">
        <!-- Left Side -->
        <div class="relative">
          <p
            class="text-blue-500 text-sm font-medium mb-4 flex items-center gap-2"
          >
            <span class="w-8 h-px bg-blue-500"></span>
            About Me
          </p>

          <h2 class="text-3xl md:text-4xl mb-6 text-white leading-tight">
            <span class="highlight-text">Software Engineer</span> focused on
            building scalable and clean digital products.
          </h2>

          <p class="text-zinc-400 leading-relaxed mb-6 text-lg">
            I graduated from Damascus University in 2025 with a specialization
            in Software Engineering. I build production-ready mobile
            applications using Flutter and modern dashboards using Vue 3.
          </p>

          <p class="text-zinc-400 leading-relaxed text-lg">
            My approach is centered around clean architecture, maintainable
            code, and modern UI/UX. I enjoy solving real-world problems and
            turning ideas into reliable software systems.
          </p>

          <!-- Decorative quote -->
          <blockquote class="mt-8 pl-4 border-l-2 border-blue-500/50">
            <p class="text-zinc-500 italic">
              "Building software that makes a difference, one line at a time."
            </p>
          </blockquote>
        </div>

        <!-- Right Side - Stats Cards -->
        <div
          class="stats-card bg-zinc-900/50 border border-zinc-800 rounded-2xl p-8 relative overflow-hidden"
        >
          <!-- Subtle ambient glow -->
          <div
            class="absolute -top-16 -right-16 w-32 h-32 bg-blue-500/10 rounded-full blur-2xl animate-pulse"
          ></div>
          <div
            class="absolute -bottom-16 -left-16 w-32 h-32 bg-blue-500/10 rounded-full blur-2xl animate-pulse"
            style="animation-delay: 1.5s"
          ></div>

          <!-- Hover glow effect -->
          <div
            class="absolute inset-0 bg-linear-to-r from-blue-500/0 via-blue-500/5 to-blue-500/0 opacity-0 stats-glow"
          ></div>

          <div class="grid grid-cols-2 gap-6 text-center relative z-10">
            <div
              class="stat-card p-6 rounded-xl hover:bg-zinc-800/50 transition-all duration-300 cursor-default group"
            >
              <div
                class="w-12 h-12 mx-auto mb-3 bg-blue-500/10 rounded-xl flex items-center justify-center group-hover:bg-blue-500/20 transition-colors"
              >
                <svg
                  class="w-6 h-6 text-blue-500"
                  fill="none"
                  stroke="currentColor"
                  viewBox="0 0 24 24"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"
                  />
                </svg>
              </div>
              <p class="text-4xl font-bold text-white">2+</p>
              <p class="text-zinc-500 text-sm mt-2">Years Experience</p>
            </div>

            <div
              class="stat-card p-6 rounded-xl hover:bg-zinc-800/50 transition-all duration-300 cursor-default group"
            >
              <div
                class="w-12 h-12 mx-auto mb-3 bg-blue-500/10 rounded-xl flex items-center justify-center group-hover:bg-blue-500/20 transition-colors"
              >
                <svg
                  class="w-6 h-6 text-blue-500"
                  fill="none"
                  stroke="currentColor"
                  viewBox="0 0 24 24"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M4 5a1 1 0 011-1h14a1 1 0 011 1v2a1 1 0 01-1 1H5a1 1 0 01-1-1V5zM4 13a1 1 0 011-1h6a1 1 0 011 1v6a1 1 0 01-1 1H5a1 1 0 01-1-1v-6zM16 13a1 1 0 011-1h2a1 1 0 011 1v6a1 1 0 01-1 1h-2a1 1 0 01-1-1v-6z"
                  />
                </svg>
              </div>
              <p class="text-4xl font-bold text-white">5+</p>
              <p class="text-zinc-500 text-sm mt-2">Projects Built</p>
            </div>

            <div
              class="stat-card p-6 rounded-xl hover:bg-zinc-800/50 transition-all duration-300 cursor-default group"
            >
              <div
                class="w-12 h-12 mx-auto mb-3 bg-blue-500/10 rounded-xl flex items-center justify-center group-hover:bg-blue-500/20 transition-colors"
              >
                <svg
                  class="w-6 h-6 text-blue-500"
                  fill="none"
                  stroke="currentColor"
                  viewBox="0 0 24 24"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14a2 2 0 01-2 2h-2a2 2 0 01-2-2z"
                  />
                </svg>
              </div>
              <p class="text-4xl font-bold text-white">2</p>
              <p class="text-zinc-500 text-sm mt-2">Dashboards</p>
            </div>

            <div
              class="stat-card p-6 rounded-xl hover:bg-zinc-800/50 transition-all duration-300 cursor-default group"
            >
              <div
                class="w-12 h-12 mx-auto mb-3 bg-blue-500/10 rounded-xl flex items-center justify-center group-hover:bg-blue-500/20 transition-colors"
              >
                <svg
                  class="w-6 h-6 text-blue-500"
                  fill="none"
                  stroke="currentColor"
                  viewBox="0 0 24 24"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M12 18h.01M8 21h8a2 2 0 002-2V5a2 2 0 00-2-2H8a2 2 0 00-2 2v14a2 2 0 002 2z"
                  />
                </svg>
              </div>
              <p class="text-4xl font-bold text-white">5</p>
              <p class="text-zinc-500 text-sm mt-2">Mobile Apps</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.stat-card {
  transform: translateY(0);
  transition: transform 0.3s ease;
}

.stat-card:hover {
  transform: translateY(-2px);
}

.stats-card {
  transition: all 0.3s ease;
}

.stats-card:hover {
  border-color: rgba(59, 130, 246, 0.4);
  box-shadow: 0 0 30px rgba(59, 130, 246, 0.15);
}

.stats-glow {
  transition: opacity 0.3s ease;
}

.stats-card:hover .stats-glow {
  opacity: 1;
}

.highlight-text {
  background: linear-gradient(135deg, #3b82f6 0%, #60a5fa 50%, #3b82f6 100%);
  background-size: 200% auto;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  animation: gradient-shift 3s ease-in-out infinite;
}

@keyframes gradient-shift {
  0%,
  100% {
    background-position: 0% center;
  }
  50% {
    background-position: 100% center;
  }
}
</style>
