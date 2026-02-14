<template>
  <section id="projects" class="section-padding bg-zinc-950">
    <div class="container-custom">
      <!-- Section Header -->
      <div class="text-center mb-20">
        <p class="text-blue-500 text-sm font-medium mb-4">Projects</p>
        <h2 class="text-3xl md:text-4xl text-white">Selected Work</h2>
        <p class="text-zinc-500 mt-4 max-w-2xl mx-auto text-sm">
          A selection of production-level applications and dashboards I've built
          using modern technologies and clean architecture principles.
        </p>
      </div>

      <!-- Project Cards -->
      <div class="space-y-24">
        <!-- TruckLink -->
        <div class="grid md:grid-cols-2 gap-12 items-center">
          <!-- Text -->
          <div>
            <h3
              class="text-2xl text-white mb-4 group-hover:text-blue-400 transition-colors duration-300"
            >
              TruckLink Platform
            </h3>

            <p class="text-zinc-400 leading-relaxed mb-6">
              A logistics platform connecting factories with transport
              companies. Includes web dashboards, driver mobile app, real-time
              tracking, and role-based system management.
            </p>

            <!-- Tech Stack -->
            <div class="flex flex-wrap gap-2 mb-6">
              <span
                class="px-3 py-1 bg-zinc-900/80 border border-zinc-800 rounded-full text-zinc-400 text-xs hover:border-blue-500/50 hover:text-blue-400 transition-colors duration-300"
                >Flutter</span
              >
              <span
                class="px-3 py-1 bg-zinc-900/80 border border-zinc-800 rounded-full text-zinc-400 text-xs hover:border-blue-500/50 hover:text-blue-400 transition-colors duration-300"
                >Vue 3</span
              >
              <span
                class="px-3 py-1 bg-zinc-900/80 border border-zinc-800 rounded-full text-zinc-400 text-xs hover:border-blue-500/50 hover:text-blue-400 transition-colors duration-300"
                >WebSocket</span
              >
              <span
                class="px-3 py-1 bg-zinc-900/80 border border-zinc-800 rounded-full text-zinc-400 text-xs hover:border-blue-500/50 hover:text-blue-400 transition-colors duration-300"
                >GPS Tracking</span
              >
              <span
                class="px-3 py-1 bg-zinc-900/80 border border-zinc-800 rounded-full text-zinc-400 text-xs hover:border-blue-500/50 hover:text-blue-400 transition-colors duration-300"
                >Clean Architecture</span
              >
            </div>

            <!-- Buttons -->
            <div class="flex gap-4">
              <a
                href="#"
                class="px-5 py-2 bg-blue-500 text-white rounded-lg hover:bg-blue-600 hover:shadow-lg hover:shadow-blue-500/25 transition-all duration-300 transform hover:-translate-y-0.5 text-sm"
              >
                View Code
              </a>
              <a
                href="#"
                class="px-5 py-2 border border-zinc-700 text-zinc-300 rounded-lg hover:border-blue-500 hover:text-blue-500 hover:bg-zinc-800/50 transition-all duration-300 text-sm"
              >
                Live Demo
              </a>
            </div>
          </div>

          <!-- Visual Placeholder -->
          <div
            class="project-card group bg-zinc-900/50 border border-zinc-800 rounded-2xl h-64 md:h-80 flex items-center justify-center text-zinc-600 overflow-hidden relative"
          >
            <!-- Ambient glow -->
            <div
              class="absolute -top-12 -right-12 w-24 h-24 bg-blue-500/10 rounded-full blur-xl"
            ></div>
            <div
              class="absolute -bottom-12 -left-12 w-24 h-24 bg-blue-500/10 rounded-full blur-xl"
            ></div>
            <div
              class="absolute inset-0 bg-linear-to-br from-blue-500/5 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-500"
            ></div>
            <div class="text-center relative z-10">
              <div
                class="w-16 h-16 mx-auto mb-4 bg-zinc-800 rounded-2xl flex items-center justify-center group-hover:scale-110 transition-transform duration-300"
              >
                <svg
                  class="w-8 h-8 text-zinc-500 group-hover:text-blue-400 transition-colors duration-300"
                  fill="none"
                  stroke="currentColor"
                  viewBox="0 0 24 24"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="1.5"
                    d="M9.75 17L9 20l-1 1h8l-1-1-.75-3M3 13h18M5 17h14a2 2 0 002-2V5a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"
                  />
                </svg>
              </div>
              <span
                class="text-sm group-hover:text-zinc-400 transition-colors duration-300"
                >Project Preview</span
              >
            </div>
          </div>
        </div>

        <!-- eSchool -->
        <div class="grid md:grid-cols-2 gap-12 items-center">
          <!-- Visual Placeholder -->
          <div
            class="project-card group bg-zinc-900/50 border border-zinc-800 rounded-2xl h-64 md:h-80 flex items-center justify-center text-zinc-600 overflow-hidden relative order-1 md:order-0"
          >
            <!-- Ambient glow -->
            <div
              class="absolute -top-12 -right-12 w-24 h-24 bg-blue-500/10 rounded-full blur-xl"
            ></div>
            <div
              class="absolute -bottom-12 -left-12 w-24 h-24 bg-blue-500/10 rounded-full blur-xl"
            ></div>
            <div
              class="absolute inset-0 bg-linear-to-br from-blue-500/5 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-500"
            ></div>
            <div class="text-center relative z-10">
              <div
                class="w-16 h-16 mx-auto mb-4 bg-zinc-800 rounded-2xl flex items-center justify-center group-hover:scale-110 transition-transform duration-300"
              >
                <svg
                  class="w-8 h-8 text-zinc-500 group-hover:text-blue-400 transition-colors duration-300"
                  fill="none"
                  stroke="currentColor"
                  viewBox="0 0 24 24"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="1.5"
                    d="M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.747 0 3.332.477 4.5 1.253v13C19.832 18.477 18.247 18 16.5 18c-1.746 0-3.332.477-4.5 1.253"
                  />
                </svg>
              </div>
              <span
                class="text-sm group-hover:text-zinc-400 transition-colors duration-300"
                >Project Preview</span
              >
            </div>
          </div>

          <!-- Text -->
          <div>
            <h3
              class="text-2xl text-white mb-4 group-hover:text-blue-400 transition-colors duration-300"
            >
              eSchool System
            </h3>

            <p class="text-zinc-400 leading-relaxed mb-6">
              Educational platform including student and teacher mobile apps,
              and an admin dashboard for managing school operations. Designed
              and developed with focus on usability and performance.
            </p>

            <!-- Tech Stack -->
            <div class="flex flex-wrap gap-2 mb-6">
              <span
                class="px-3 py-1 bg-zinc-900/80 border border-zinc-800 rounded-full text-zinc-400 text-xs hover:border-blue-500/50 hover:text-blue-400 transition-colors duration-300"
                >Flutter</span
              >
              <span
                class="px-3 py-1 bg-zinc-900/80 border border-zinc-800 rounded-full text-zinc-400 text-xs hover:border-blue-500/50 hover:text-blue-400 transition-colors duration-300"
                >Vue Dashboard</span
              >
              <span
                class="px-3 py-1 bg-zinc-900/80 border border-zinc-800 rounded-full text-zinc-400 text-xs hover:border-blue-500/50 hover:text-blue-400 transition-colors duration-300"
                >Laravel API</span
              >
              <span
                class="px-3 py-1 bg-zinc-900/80 border border-zinc-800 rounded-full text-zinc-400 text-xs hover:border-blue-500/50 hover:text-blue-400 transition-colors duration-300"
                >REST</span
              >
              <span
                class="px-3 py-1 bg-zinc-900/80 border border-zinc-800 rounded-full text-zinc-400 text-xs hover:border-blue-500/50 hover:text-blue-400 transition-colors duration-300"
                >UI Design (Figma)</span
              >
            </div>

            <!-- Buttons -->
            <div class="flex gap-4">
              <a
                href="#"
                class="px-5 py-2 bg-blue-500 text-white rounded-lg hover:bg-blue-600 hover:shadow-lg hover:shadow-blue-500/25 transition-all duration-300 transform hover:-translate-y-0.5 text-sm"
              >
                View Code
              </a>
              <a
                href="#"
                class="px-5 py-2 border border-zinc-700 text-zinc-300 rounded-lg hover:border-blue-500 hover:text-blue-500 hover:bg-zinc-800/50 transition-all duration-300 text-sm"
              >
                Live Demo
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.project-card {
  transition: all 0.3s ease;
}

.project-card:hover {
  border-color: rgba(59, 130, 246, 0.3);
  transform: translateY(-2px);
}
</style>
