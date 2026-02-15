<template>
  <section id="about" class="section-padding bg-zinc-950">
    <div class="container-custom">
      <div class="grid md:grid-cols-2 gap-16 items-center">
        <!-- Left Side -->
        <div>
          <p class="text-blue-500 text-sm font-medium mb-4">About Me</p>

          <h2 class="text-3xl md:text-4xl mb-6 text-white">
            <span class="highlight-text">Software Engineer</span> focused on
            building scalable and clean digital products.
          </h2>

          <p class="text-zinc-400 leading-relaxed mb-6">
            I graduated from Damascus University in 2025 with a specialization
            in Software Engineering. I build production-ready mobile
            applications using Flutter and modern dashboards using Vue 3.
          </p>

          <p class="text-zinc-400 leading-relaxed">
            My approach is centered around clean architecture, maintainable
            code, and modern UI/UX. I enjoy solving real-world problems and
            turning ideas into reliable software systems.
          </p>
        </div>

        <!-- Right Side -->
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
          <div class="grid grid-cols-2 gap-6 text-center">
            <div
              class="stat-card p-4 rounded-xl hover:bg-zinc-800/50 transition-all duration-300 cursor-default"
            >
              <p class="text-3xl font-semibold text-white">2+</p>
              <p class="text-zinc-500 text-sm mt-2">Years Experience</p>
            </div>

            <div
              class="stat-card p-4 rounded-xl hover:bg-zinc-800/50 transition-all duration-300 cursor-default"
            >
              <p class="text-3xl font-semibold text-white">5+</p>
              <p class="text-zinc-500 text-sm mt-2">Projects Built</p>
            </div>

            <div
              class="stat-card p-4 rounded-xl hover:bg-zinc-800/50 transition-all duration-300 cursor-default"
            >
              <p class="text-3xl font-semibold text-white">3</p>
              <p class="text-zinc-500 text-sm mt-2">Dashboards</p>
            </div>

            <div
              class="stat-card p-4 rounded-xl hover:bg-zinc-800/50 transition-all duration-300 cursor-default"
            >
              <p class="text-3xl font-semibold text-white">4</p>
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
