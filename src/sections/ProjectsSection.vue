<template>
  <section id="projects" class="section-padding bg-zinc-950">
    <!-- Lightbox Modal -->
    <div
      v-if="lightboxOpen"
      class="fixed inset-0 z-50 flex items-center justify-center bg-black/90 backdrop-blur-sm"
      @click="closeLightbox"
    >
      <button
        class="absolute top-4 right-4 text-white hover:text-blue-400 transition-colors p-2"
        @click="closeLightbox"
      >
        <svg
          class="w-8 h-8"
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
      <img
        :src="lightboxImage"
        alt="Enlarged view"
        class="max-w-[90vw] max-h-[90vh] object-contain rounded-lg shadow-2xl"
        @click.stop
      />
    </div>

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
        <!-- Do Re Mi -->
        <div class="grid md:grid-cols-2 gap-12 items-center">
          <!-- Text -->
          <div>
            <h3
              class="text-2xl text-white mb-4 group-hover:text-blue-400 transition-colors duration-300"
            >
              Do Re Mi
            </h3>

            <p class="text-zinc-400 leading-relaxed mb-6">
              A music learning platform with interactive lessons, progress
              tracking, and real-time feedback. Features include video
              tutorials, practice exercises, and achievement system.
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
                >Firebase</span
              >
              <span
                class="px-3 py-1 bg-zinc-900/80 border border-zinc-800 rounded-full text-zinc-400 text-xs hover:border-blue-500/50 hover:text-blue-400 transition-colors duration-300"
                >Audio Processing</span
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

          <!-- Mockup Gallery -->
          <div class="space-y-4">
            <!-- Video Container -->
            <div
              class="relative rounded-2xl overflow-hidden border border-zinc-800 bg-zinc-900 aspect-video group"
            >
              <video
                class="w-full h-full object-cover"
                autoplay
                muted
                loop
                playsinline
              >
                <source src="/mockups/doremi.mp4" type="video/mp4" />
              </video>
              <!-- Video overlay for hover -->
              <div
                class="absolute inset-0 bg-gradient-to-t from-black/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-4 pointer-events-none"
              >
                <span class="text-white text-sm font-medium">Watch Demo</span>
              </div>
            </div>

            <!-- Mockup Images Grid -->
            <div class="grid grid-cols-3 gap-4">
              <!-- Mockup 1 -->
              <div
                class="relative rounded-xl overflow-hidden border border-zinc-800 bg-zinc-900 aspect-square group"
              >
                <img
                  src="/mockups/doremi1.png"
                  alt="Do Re Mi App"
                  class="w-full h-full object-cover cursor-pointer"
                  @click="openLightbox('/mockups/doremi1.png')"
                />
                <div
                  class="absolute inset-0 bg-gradient-to-t from-black/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-2 pointer-events-none"
                >
                  <span class="text-white text-xs font-medium">Screen 1</span>
                </div>
              </div>

              <!-- Mockup 2 -->
              <div
                class="relative rounded-xl overflow-hidden border border-zinc-800 bg-zinc-900 aspect-square group"
              >
                <img
                  src="/mockups/doremi2.png"
                  alt="Do Re Mi Lessons"
                  class="w-full h-full object-cover cursor-pointer"
                  @click="openLightbox('/mockups/doremi2.png')"
                />
                <div
                  class="absolute inset-0 bg-gradient-to-t from-black/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-2 pointer-events-none"
                >
                  <span class="text-white text-xs font-medium">Screen 2</span>
                </div>
              </div>

              <!-- Mockup 3 -->
              <div
                class="relative rounded-xl overflow-hidden border border-zinc-800 bg-zinc-900 aspect-square group"
              >
                <img
                  src="/mockups/doremi3.jpg"
                  alt="Do Re Mi Features"
                  class="w-full h-full object-cover cursor-pointer"
                  @click="openLightbox('/mockups/doremi3.jpg')"
                />
                <div
                  class="absolute inset-0 bg-gradient-to-t from-black/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-2 pointer-events-none"
                >
                  <span class="text-white text-xs font-medium">Screen 3</span>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- eSchool -->
        <div class="grid md:grid-cols-2 gap-12 items-center">
          <!-- Mockup Gallery -->
          <div class="space-y-4 order-1 md:order-0">
            <!-- Video Container -->
            <div
              class="relative rounded-2xl overflow-hidden border border-zinc-800 bg-zinc-900 aspect-video group"
            >
              <video
                class="w-full h-full object-cover"
                autoplay
                muted
                loop
                playsinline
              >
                <source src="/mockups/eschool.mp4" type="video/mp4" />
              </video>
              <!-- Video overlay for hover -->
              <div
                class="absolute inset-0 bg-gradient-to-t from-black/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-4 pointer-events-none"
              >
                <span class="text-white text-sm font-medium">Watch Demo</span>
              </div>
            </div>

            <!-- Mockup Images Grid -->
            <div class="grid grid-cols-3 gap-4">
              <!-- Mockup 1 -->
              <div
                class="relative rounded-xl overflow-hidden border border-zinc-800 bg-zinc-900 aspect-square group"
              >
                <img
                  src="/mockups/eschool1.png"
                  alt="eSchool Screen 1"
                  class="w-full h-full object-cover cursor-pointer"
                  @click="openLightbox('/mockups/eschool1.png')"
                />
                <div
                  class="absolute inset-0 bg-gradient-to-t from-black/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-2 pointer-events-none"
                >
                  <span class="text-white text-xs font-medium">Screen 1</span>
                </div>
              </div>

              <!-- Mockup 2 -->
              <div
                class="relative rounded-xl overflow-hidden border border-zinc-800 bg-zinc-900 aspect-square group"
              >
                <img
                  src="/mockups/eschool2.png"
                  alt="eSchool Screen 2"
                  class="w-full h-full object-cover cursor-pointer"
                  @click="openLightbox('/mockups/eschool2.png')"
                />
                <div
                  class="absolute inset-0 bg-gradient-to-t from-black/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-2 pointer-events-none"
                >
                  <span class="text-white text-xs font-medium">Screen 2</span>
                </div>
              </div>

              <!-- Mockup 3 -->
              <div
                class="relative rounded-xl overflow-hidden border border-zinc-800 bg-zinc-900 aspect-square group"
              >
                <img
                  src="/mockups/eschool3.jpg"
                  alt="eSchool Screen 3"
                  class="w-full h-full object-cover cursor-pointer"
                  @click="openLightbox('/mockups/eschool3.jpg')"
                />
                <div
                  class="absolute inset-0 bg-gradient-to-t from-black/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-2 pointer-events-none"
                >
                  <span class="text-white text-xs font-medium">Screen 3</span>
                </div>
              </div>
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

          <!-- Mockup Gallery -->
          <div class="space-y-4">
            <!-- Video Container -->
            <div
              class="relative rounded-2xl overflow-hidden border border-zinc-800 bg-zinc-900 aspect-video group"
            >
              <video
                class="w-full h-full object-cover"
                autoplay
                muted
                loop
                playsinline
              >
                <source src="/mockups/trucklink.mp4" type="video/mp4" />
              </video>
              <!-- Video overlay for hover -->
              <div
                class="absolute inset-0 bg-gradient-to-t from-black/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-4 pointer-events-none"
              >
                <span class="text-white text-sm font-medium">Watch Demo</span>
              </div>
            </div>

            <!-- Mockup Images Grid -->
            <div class="grid grid-cols-3 gap-4">
              <!-- Mockup 1 -->
              <div
                class="relative rounded-xl overflow-hidden border border-zinc-800 bg-zinc-900 aspect-square group"
              >
                <img
                  src="/mockups/placeholder.svg"
                  alt="TruckLink Screen 1"
                  class="w-full h-full object-cover cursor-pointer"
                  @click="openLightbox('/mockups/placeholder.svg')"
                />
                <div
                  class="absolute inset-0 bg-gradient-to-t from-black/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-2 pointer-events-none"
                >
                  <span class="text-white text-xs font-medium">Screen 1</span>
                </div>
              </div>

              <!-- Mockup 2 -->
              <div
                class="relative rounded-xl overflow-hidden border border-zinc-800 bg-zinc-900 aspect-square group"
              >
                <img
                  src="/mockups/placeholder.svg"
                  alt="TruckLink Screen 2"
                  class="w-full h-full object-cover cursor-pointer"
                  @click="openLightbox('/mockups/placeholder.svg')"
                />
                <div
                  class="absolute inset-0 bg-gradient-to-t from-black/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-2 pointer-events-none"
                >
                  <span class="text-white text-xs font-medium">Screen 2</span>
                </div>
              </div>

              <!-- Mockup 3 -->
              <div
                class="relative rounded-xl overflow-hidden border border-zinc-800 bg-zinc-900 aspect-square group"
              >
                <img
                  src="/mockups/placeholder.svg"
                  alt="TruckLink Screen 3"
                  class="w-full h-full object-cover cursor-pointer"
                  @click="openLightbox('/mockups/placeholder.svg')"
                />
                <div
                  class="absolute inset-0 bg-gradient-to-t from-black/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-2 pointer-events-none"
                >
                  <span class="text-white text-xs font-medium">Screen 3</span>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Emaniyat -->
        <div class="grid md:grid-cols-2 gap-12 items-center">
          <!-- Mockup Gallery -->
          <div class="space-y-4 order-1 md:order-0">
            <!-- Video Container -->
            <div
              class="relative rounded-2xl overflow-hidden border border-zinc-800 bg-zinc-900 aspect-video group"
            >
              <video
                class="w-full h-full object-cover"
                autoplay
                muted
                loop
                playsinline
              >
                <source src="/mockups/emaniyat.mp4" type="video/mp4" />
              </video>
              <!-- Video overlay for hover -->
              <div
                class="absolute inset-0 bg-gradient-to-t from-black/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-4 pointer-events-none"
              >
                <span class="text-white text-sm font-medium">Watch Demo</span>
              </div>
            </div>

            <!-- Mockup Images Grid -->
            <div class="grid grid-cols-3 gap-4">
              <!-- Mockup 1 -->
              <div
                class="relative rounded-xl overflow-hidden border border-zinc-800 bg-zinc-900 aspect-square group"
              >
                <img
                  src="/mockups/emaniyat1.png"
                  alt="Emaniyat Screen 1"
                  class="w-full h-full object-cover cursor-pointer"
                  @click="openLightbox('/mockups/emaniyat1.png')"
                />
                <div
                  class="absolute inset-0 bg-gradient-to-t from-black/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-2 pointer-events-none"
                >
                  <span class="text-white text-xs font-medium">Screen 1</span>
                </div>
              </div>

              <!-- Mockup 2 -->
              <div
                class="relative rounded-xl overflow-hidden border border-zinc-800 bg-zinc-900 aspect-square group"
              >
                <img
                  src="/mockups/emaniyat2.png"
                  alt="Emaniyat Screen 2"
                  class="w-full h-full object-cover cursor-pointer"
                  @click="openLightbox('/mockups/emaniyat2.png')"
                />
                <div
                  class="absolute inset-0 bg-gradient-to-t from-black/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-2 pointer-events-none"
                >
                  <span class="text-white text-xs font-medium">Screen 2</span>
                </div>
              </div>

              <!-- Mockup 3 -->
              <div
                class="relative rounded-xl overflow-hidden border border-zinc-800 bg-zinc-900 aspect-square group"
              >
                <img
                  src="/mockups/emaniyat3.png"
                  alt="Emaniyat Screen 3"
                  class="w-full h-full object-cover cursor-pointer"
                  @click="openLightbox('/mockups/emaniyat3.png')"
                />
                <div
                  class="absolute inset-0 bg-gradient-to-t from-black/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-2 pointer-events-none"
                >
                  <span class="text-white text-xs font-medium">Screen 3</span>
                </div>
              </div>
            </div>
          </div>

          <!-- Text -->
          <div>
            <h3
              class="text-2xl text-white mb-4 group-hover:text-blue-400 transition-colors duration-300"
            >
              Emaniyat
            </h3>

            <p class="text-zinc-400 leading-relaxed mb-6">
              A comprehensive platform for managing religious events and
              gatherings. Includes event scheduling, participant management,
              notifications, and reporting features.
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
                >Node.js</span
              >
              <span
                class="px-3 py-1 bg-zinc-900/80 border border-zinc-800 rounded-full text-zinc-400 text-xs hover:border-blue-500/50 hover:text-blue-400 transition-colors duration-300"
                >PostgreSQL</span
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

<script setup lang="ts">
import { ref } from "vue";

const lightboxOpen = ref(false);
const lightboxImage = ref("");

const openLightbox = (imageSrc: string) => {
  lightboxImage.value = imageSrc;
  lightboxOpen.value = true;
  document.body.style.overflow = "hidden";
};

const closeLightbox = () => {
  lightboxOpen.value = false;
  lightboxImage.value = "";
  document.body.style.overflow = "";
};
</script>
