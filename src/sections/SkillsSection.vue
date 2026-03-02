<template>
  <section
    id="skills"
    class="section-padding bg-zinc-900 relative overflow-hidden"
  >
    <!-- Background decorations -->
    <div
      class="absolute top-20 left-0 w-64 h-64 bg-blue-500/5 rounded-full blur-3xl"
    ></div>
    <div
      class="absolute bottom-20 right-0 w-64 h-64 bg-blue-500/5 rounded-full blur-3xl"
    ></div>

    <div class="container-custom relative z-10">
      <div class="text-center mb-16">
        <p
          class="text-blue-500 text-sm font-medium mb-4 flex items-center justify-center gap-2"
        >
          <span class="w-8 h-px bg-blue-500"></span>
          Skills
          <span class="w-8 h-px bg-blue-500"></span>
        </p>
        <h2 class="text-3xl md:text-4xl text-white mb-4">
          Technologies I Work With
        </h2>
        <p class="text-zinc-500 max-w-xl mx-auto">
          Building robust and scalable solutions with modern technologies and
          best practices.
        </p>
      </div>

      <div class="grid md:grid-cols-3 gap-6">
        <!-- Mobile -->
        <div
          class="skill-card group bg-zinc-950 border border-zinc-800 rounded-2xl p-8 hover:border-blue-500/30 hover:shadow-xl hover:shadow-blue-500/5 transition-all duration-500 relative overflow-hidden"
        >
          <!-- Gradient overlay on hover -->
          <div
            class="absolute inset-0 bg-linear-to-br from-blue-500/5 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-500"
          ></div>

          <div
            class="w-14 h-14 bg-zinc-900 rounded-2xl flex items-center justify-center mb-6 group-hover:bg-blue-500/10 transition-colors duration-300 relative z-10"
          >
            <svg
              class="w-7 h-7 text-blue-500"
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
          <h3 class="text-white text-xl mb-4 font-semibold relative z-10">
            Mobile Development
          </h3>
          <ul class="space-y-3 text-zinc-400 text-sm relative z-10">
            <li
              class="flex items-center gap-3 group-hover:translate-x-1 transition-transform duration-300"
            >
              <span class="w-1.5 h-1.5 bg-blue-500 rounded-full"></span>
              Flutter & Dart
            </li>
            <li
              class="flex items-center gap-3 group-hover:translate-x-1 transition-transform duration-300"
            >
              <span class="w-1.5 h-1.5 bg-blue-500 rounded-full"></span>
              Clean Architecture
            </li>
            <li
              class="flex items-center gap-3 group-hover:translate-x-1 transition-transform duration-300"
            >
              <span class="w-1.5 h-1.5 bg-blue-500 rounded-full"></span>
              Animations
            </li>
            <li
              class="flex items-center gap-3 group-hover:translate-x-1 transition-transform duration-300"
            >
              <span class="w-1.5 h-1.5 bg-blue-500 rounded-full"></span>
              WebSocket Integration
            </li>
            <li
              class="flex items-center gap-3 group-hover:translate-x-1 transition-transform duration-300"
            >
              <span class="w-1.5 h-1.5 bg-blue-500 rounded-full"></span>
              GPS & Background Services
            </li>
            <li
              class="flex items-center gap-3 group-hover:translate-x-1 transition-transform duration-300"
            >
              <span class="w-1.5 h-1.5 bg-blue-500 rounded-full"></span>
              State Management (BLoC, GetX)
            </li>
          </ul>
        </div>

        <!-- Frontend -->
        <div
          class="skill-card group bg-zinc-950 border border-zinc-800 rounded-2xl p-8 hover:border-blue-500/30 hover:shadow-xl hover:shadow-blue-500/5 transition-all duration-500 relative overflow-hidden"
        >
          <!-- Gradient overlay on hover -->
          <div
            class="absolute inset-0 bg-linear-to-br from-blue-500/5 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-500"
          ></div>

          <div
            class="w-14 h-14 bg-zinc-900 rounded-2xl flex items-center justify-center mb-6 group-hover:bg-blue-500/10 transition-colors duration-300 relative z-10"
          >
            <svg
              class="w-7 h-7 text-blue-500"
              fill="none"
              stroke="currentColor"
              viewBox="0 0 24 24"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M9.75 17L9 20l-1 1h8l-1-1-.75-3M3 13h18M5 17h14a2 2 0 002-2V5a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"
              />
            </svg>
          </div>
          <h3 class="text-white text-xl mb-4 font-semibold relative z-10">
            Frontend Development
          </h3>
          <ul class="space-y-3 text-zinc-400 text-sm relative z-10">
            <li
              class="flex items-center gap-3 group-hover:translate-x-1 transition-transform duration-300"
            >
              <span class="w-1.5 h-1.5 bg-blue-500 rounded-full"></span>
              Vue 3 & Vite
            </li>
            <li
              class="flex items-center gap-3 group-hover:translate-x-1 transition-transform duration-300"
            >
              <span class="w-1.5 h-1.5 bg-blue-500 rounded-full"></span>
              TypeScript
            </li>
            <li
              class="flex items-center gap-3 group-hover:translate-x-1 transition-transform duration-300"
            >
              <span class="w-1.5 h-1.5 bg-blue-500 rounded-full"></span>
              Tailwind CSS
            </li>
            <li
              class="flex items-center gap-3 group-hover:translate-x-1 transition-transform duration-300"
            >
              <span class="w-1.5 h-1.5 bg-blue-500 rounded-full"></span>
              Pinia
            </li>
            <li
              class="flex items-center gap-3 group-hover:translate-x-1 transition-transform duration-300"
            >
              <span class="w-1.5 h-1.5 bg-blue-500 rounded-full"></span>
              Axios
            </li>
            <li
              class="flex items-center gap-3 group-hover:translate-x-1 transition-transform duration-300"
            >
              <span class="w-1.5 h-1.5 bg-blue-500 rounded-full"></span>
              Responsive Design
            </li>
          </ul>
        </div>

        <!-- Tools -->
        <div
          class="skill-card group bg-zinc-950 border border-zinc-800 rounded-2xl p-8 hover:border-blue-500/30 hover:shadow-xl hover:shadow-blue-500/5 transition-all duration-500 relative overflow-hidden"
        >
          <!-- Gradient overlay on hover -->
          <div
            class="absolute inset-0 bg-linear-to-br from-blue-500/5 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-500"
          ></div>

          <div
            class="w-14 h-14 bg-zinc-900 rounded-2xl flex items-center justify-center mb-6 group-hover:bg-blue-500/10 transition-colors duration-300 relative z-10"
          >
            <svg
              class="w-7 h-7 text-blue-500"
              fill="none"
              stroke="currentColor"
              viewBox="0 0 24 24"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M10.325 4.317c.426-1.756 2.924-1.756 3.35 0a1.724 1.724 0 002.573 1.066c1.543-.94 3.31.826 2.37 2.37a1.724 1.724 0 001.065 2.572c1.756.426 1.756 2.924 0 3.35a1.724 1.724 0 00-1.066 2.573c.94 1.543-.826 3.31-2.37 2.37a1.724 1.724 0 00-2.572 1.065c-.426 1.756-2.924 1.756-3.35 0a1.724 1.724 0 00-2.573-1.066c-1.543.94-3.31-.826-2.37-2.37a1.724 1.724 0 00-1.065-2.572c-1.756-.426-1.756-2.924 0-3.35a1.724 1.724 0 001.066-2.573c-.94-1.543.826-3.31 2.37-2.37.996.608 2.296.07 2.572-1.065z"
              />
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"
              />
            </svg>
          </div>
          <h3 class="text-white text-xl mb-4 font-semibold relative z-10">
            Tools & Practices
          </h3>
          <ul class="space-y-3 text-zinc-400 text-sm relative z-10">
            <li
              class="flex items-center gap-3 group-hover:translate-x-1 transition-transform duration-300"
            >
              <span class="w-1.5 h-1.5 bg-blue-500 rounded-full"></span>
              Git & GitHub
            </li>
            <li
              class="flex items-center gap-3 group-hover:translate-x-1 transition-transform duration-300"
            >
              <span class="w-1.5 h-1.5 bg-blue-500 rounded-full"></span>
              Figma (UI Design)
            </li>
            <li
              class="flex items-center gap-3 group-hover:translate-x-1 transition-transform duration-300"
            >
              <span class="w-1.5 h-1.5 bg-blue-500 rounded-full"></span>
              REST APIs
            </li>
            <li
              class="flex items-center gap-3 group-hover:translate-x-1 transition-transform duration-300"
            >
              <span class="w-1.5 h-1.5 bg-blue-500 rounded-full"></span>
              Deployment & CI/CD
            </li>
            <li
              class="flex items-center gap-3 group-hover:translate-x-1 transition-transform duration-300"
            >
              <span class="w-1.5 h-1.5 bg-blue-500 rounded-full"></span>
              Clean Code Principles + SOLID Principles
            </li>
            <li
              class="flex items-center gap-3 group-hover:translate-x-1 transition-transform duration-300"
            >
              <span class="w-1.5 h-1.5 bg-blue-500 rounded-full"></span>
              Agile Workflow
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.skill-card {
  transform: translateY(0);
  transition: transform 0.3s ease;
}

.skill-card:hover {
  transform: translateY(-4px);
}
</style>
