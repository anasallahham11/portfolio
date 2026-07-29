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
        <p
          class="text-blue-500 text-sm font-medium mb-4 flex items-center justify-center gap-2"
        >
          <span class="w-8 h-px bg-blue-500"></span>
          Projects
          <span class="w-8 h-px bg-blue-500"></span>
        </p>
        <h2 class="text-3xl md:text-4xl text-white mb-4 font-bold">
          Selected Work
        </h2>
        <p class="text-zinc-500 mt-4 max-w-2xl mx-auto text-lg">
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
              A comprehensive streaming music platform delivering an immersive
              audio experience. Features trending songs, music videos, artist
              profiles, and album collections. Includes live events, curated
              playlists, custom playlist creation, radio streaming, and
              podcasts. Offers personal library management, favorites, and
              offline downloads for uninterrupted listening anywhere.
            </p>

            <!-- Tech Stack -->
            <div class="flex flex-wrap gap-2 mb-6">
              <span
                class="px-3 py-1 bg-zinc-900/80 border border-zinc-800 rounded-full text-zinc-400 text-xs hover:border-blue-500/50 hover:text-blue-400 transition-colors duration-300"
                >Flutter</span
              >
              <span
                class="px-3 py-1 bg-zinc-900/80 border border-zinc-800 rounded-full text-zinc-400 text-xs hover:border-blue-500/50 hover:text-blue-400 transition-colors duration-300"
                >Firebase</span
              >
              <span
                class="px-3 py-1 bg-zinc-900/80 border border-zinc-800 rounded-full text-zinc-400 text-xs hover:border-blue-500/50 hover:text-blue-400 transition-colors duration-300"
                >BLoC</span
              >
            </div>

            <!-- Buttons -->
            <div class="flex gap-4">
              <a
                href="https://play.google.com/store/apps/details?id=site.rand.doremi.prod"
                target="_blank"
                class="px-5 py-2 bg-blue-500 text-white rounded-lg hover:bg-blue-600 hover:shadow-lg hover:shadow-blue-500/25 transition-all duration-300 transform hover:-translate-y-0.5 text-sm flex items-center gap-2"
              >
                <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 24 24">
                  <path
                    d="M3.609 1.814L13.792 12 3.61 22.186a.996.996 0 0 1-.61-.92V2.734a1 1 0 0 1 .609-.92zm10.89 10.893l2.302 2.302-10.937 6.333 8.635-8.635zm3.199-3.198l2.807 1.626a1 1 0 0 1 0 1.73l-2.808 1.626L15.206 12l2.492-2.491zM5.864 2.658L16.8 8.99l-2.302 2.302-8.635-8.634z"
                  />
                </svg>
                Get on Play Store
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
                class="absolute inset-0 bg-linear-to-t from-black/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-4 pointer-events-none"
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
                  class="absolute inset-0 bg-linear-to-t from-black/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-2 pointer-events-none"
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
                  class="absolute inset-0 bg-linear-to-t from-black/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-2 pointer-events-none"
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
                  class="absolute inset-0 bg-linear-to-t from-black/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-2 pointer-events-none"
                >
                  <span class="text-white text-xs font-medium">Screen 3</span>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- EduGate -->
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
                <source src="/mockups/edugate.mp4" type="video/mp4" />
              </video>
              <!-- Video overlay for hover -->
              <div
                class="absolute inset-0 bg-linear-to-t from-black/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-4 pointer-events-none"
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
                   src="/mockups/edugate1.png"
                   alt="EduGate Screen 1"
                   class="w-full h-full object-cover cursor-pointer"
                   @click="openLightbox('/mockups/edugate1.png')"
                 />
                <div
                  class="absolute inset-0 bg-linear-to-t from-black/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-2 pointer-events-none"
                >
                  <span class="text-white text-xs font-medium">Screen 1</span>
                </div>
              </div>

              <!-- Mockup 2 -->
              <div
                class="relative rounded-xl overflow-hidden border border-zinc-800 bg-zinc-900 aspect-square group"
              >
                 <img
                   src="/mockups/edugate2.png"
                   alt="EduGate Screen 2"
                   class="w-full h-full object-cover cursor-pointer"
                   @click="openLightbox('/mockups/edugate2.png')"
                 />
                <div
                  class="absolute inset-0 bg-linear-to-t from-black/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-2 pointer-events-none"
                >
                  <span class="text-white text-xs font-medium">Screen 2</span>
                </div>
              </div>

              <!-- Mockup 3 -->
              <div
                class="relative rounded-xl overflow-hidden border border-zinc-800 bg-zinc-900 aspect-square group"
              >
                 <img
                   src="/mockups/edugate3.png"
                   alt="EduGate Screen 3"
                   class="w-full h-full object-cover cursor-pointer"
                   @click="openLightbox('/mockups/edugate3.png')"
                 />
                <div
                  class="absolute inset-0 bg-linear-to-t from-black/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-2 pointer-events-none"
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
              EduGate
            </h3>

            <p class="text-zinc-400 leading-relaxed mb-6">
              A comprehensive school management system featuring a powerful
              admin dashboard alongside dedicated mobile apps for students,
              teachers, and parents. Manages student, staff, and teacher
              profiles with full attendance tracking, timetables, discipline
              records, marks, and exam management. Includes library automation,
              event organization, detailed reporting, and real-time
              notifications for seamless communication across the entire school
              community.
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
                >Firebase</span
              >
              <span
                class="px-3 py-1 bg-zinc-900/80 border border-zinc-800 rounded-full text-zinc-400 text-xs hover:border-blue-500/50 hover:text-blue-400 transition-colors duration-300"
                >Push Notifications</span
              >
            </div>

            <!-- Buttons -->
            <div class="flex gap-4">
              <span
                class="px-5 py-2 border border-zinc-700 text-zinc-500 rounded-lg text-sm cursor-not-allowed"
              >
                Coming Soon
              </span>
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
              A comprehensive logistics marketplace connecting factories with
              transport companies. Factories post shipping requests while
              companies submit competitive offers. Features real-time GPS driver
              tracking on map, shipment status monitoring, and dedicated request
              capabilities for ongoing partnerships. Includes a powerful admin
              panel for system management, complaint handling, and full
              operational monitoring, along with a dedicated mobile app for
              drivers.
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
              <span
                class="px-5 py-2 border border-zinc-700 text-zinc-500 rounded-lg text-sm cursor-not-allowed"
              >
                Coming Soon
              </span>
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
                class="absolute inset-0 bg-linear-to-t from-black/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-4 pointer-events-none"
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
                  src="/mockups/trucklink1.jpg"
                  alt="TruckLink Screen 1"
                  class="w-full h-full object-cover cursor-pointer"
                  @click="openLightbox('/mockups/trucklink1.jpg')"
                />
                <div
                  class="absolute inset-0 bg-linear-to-t from-black/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-2 pointer-events-none"
                >
                  <span class="text-white text-xs font-medium">Screen 1</span>
                </div>
              </div>

              <!-- Mockup 2 -->
              <div
                class="relative rounded-xl overflow-hidden border border-zinc-800 bg-zinc-900 aspect-square group"
              >
                <img
                  src="/mockups/trucklink2.jpg"
                  alt="TruckLink Screen 2"
                  class="w-full h-full object-cover cursor-pointer"
                  @click="openLightbox('/mockups/trucklink2.jpg')"
                />
                <div
                  class="absolute inset-0 bg-linear-to-t from-black/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-2 pointer-events-none"
                >
                  <span class="text-white text-xs font-medium">Screen 2</span>
                </div>
              </div>

              <!-- Mockup 3 -->
              <div
                class="relative rounded-xl overflow-hidden border border-zinc-800 bg-zinc-900 aspect-square group"
              >
                <img
                  src="/mockups/trucklink3.png"
                  alt="TruckLink Screen 3"
                  class="w-full h-full object-cover cursor-pointer"
                  @click="openLightbox('/mockups/trucklink3.png')"
                />
                <div
                  class="absolute inset-0 bg-linear-to-t from-black/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-2 pointer-events-none"
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
                class="absolute inset-0 bg-linear-to-t from-black/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-4 pointer-events-none"
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
                  class="absolute inset-0 bg-linear-to-t from-black/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-2 pointer-events-none"
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
                  class="absolute inset-0 bg-linear-to-t from-black/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-2 pointer-events-none"
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
                  class="absolute inset-0 bg-linear-to-t from-black/50 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-end p-2 pointer-events-none"
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
              An all-in-one Islamic application featuring Quran with multiple
              reciters, bookmark management, and downloadable ayahs. Includes
              a digital library of Islamic books with reading and download
              options. Offers daily azkar and duas, Qiblah direction finder,
              digital masbaha, Zakat calculator, nearest mosques locator, 99
              Names of Allah, and an Islamic calendar for tracking important
              dates and events.
            </p>

            <!-- Tech Stack -->
            <div class="flex flex-wrap gap-2 mb-6">
              <span
                class="px-3 py-1 bg-zinc-900/80 border border-zinc-800 rounded-full text-zinc-400 text-xs hover:border-blue-500/50 hover:text-blue-400 transition-colors duration-300"
                >Flutter</span
              >
              <span
                class="px-3 py-1 bg-zinc-900/80 border border-zinc-800 rounded-full text-zinc-400 text-xs hover:border-blue-500/50 hover:text-blue-400 transition-colors duration-300"
                >Firebase</span
              >
              <span
                class="px-3 py-1 bg-zinc-900/80 border border-zinc-800 rounded-full text-zinc-400 text-xs hover:border-blue-500/50 hover:text-blue-400 transition-colors duration-300"
                >GetX</span
              >
            </div>

            <!-- Buttons -->
            <div class="flex gap-4">
              <span
                class="px-5 py-2 border border-zinc-700 text-zinc-500 rounded-lg text-sm cursor-not-allowed"
              >
                Coming Soon
              </span>
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