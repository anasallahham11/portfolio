<template>
  <footer class="bg-zinc-950 border-t border-zinc-800 py-8">
    <div
      class="container-custom flex flex-col md:flex-row justify-between items-center text-zinc-500 text-sm"
    >
      <!-- Left -->
      <p>
        &copy; 2026 <span class="text-zinc-300">Anas Allahham</span>. All rights
        reserved.
      </p>

      <!-- Right -->
      <div class="flex gap-6 mt-4 md:mt-0">
        <a
          href="mailto:anasallahham11@gmail.com"
          class="footer-link relative hover:text-white transition-colors duration-300"
        >
          Email
        </a>
        <a
          href="https://linkedin.com/in/anasallahham11"
          target="_blank"
          class="footer-link relative hover:text-white transition-colors duration-300"
        >
          LinkedIn
        </a>
        <a
          href="https://github.com/anasallahham11"
          target="_blank"
          class="footer-link relative hover:text-white transition-colors duration-300"
        >
          GitHub
        </a>
      </div>
    </div>
  </footer>
</template>

<style scoped>
.footer-link::after {
  content: "";
  position: absolute;
  bottom: -2px;
  left: 0;
  width: 0;
  height: 1px;
  background: #3b82f6;
  transition: width 0.3s ease;
}

.footer-link:hover::after {
  width: 100%;
}
</style>
