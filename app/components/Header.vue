<script setup lang="ts">
</script>
<template>
  <header
      class="fixed top-0 w-full z-50 bg-black/20 backdrop-blur-md"
  >
    <div
        class="container mx-auto px-6 py-5"
    >

      <nav
          class="flex items-center justify-between
        rounded-2xl border border-white/10
        bg-black/40 backdrop-blur-xl
        px-6 py-4"
      >

        <!-- Logo -->
        <div
            class="w-20"
        >
          <img
              src="/images/logo.png"
              alt="Logo"
              class="w-full h-auto object-contain"
          >
        </div>


        <!-- Menu -->
        <ul
            class="hidden md:flex items-center gap-8 text-gray-300"
        >
          <li class="hover:text-blue-400">
            <a href="#">
              صفحه اصلی
            </a>
          </li>

          <li class="hover:text-blue-400">
            <a href="diesel">
              دیزل و ژنراتور
            </a>
          </li>

          <li class="hover:text-blue-400">
            <a href="#services">
              بررسی و کیوتین
            </a>
          </li>

          <li class="hover:text-blue-400">
            <a href="#services">
             پمپ و مشعل
            </a>
          </li>

          <li class="hover:text-blue-400">
            <a href="#services">
             ماشین آلات ساختمانی
            </a>
          </li>

          <li class="hover:text-blue-400">
            <a href="#about">
              درباره ما
            </a>
          </li>

          <li class="hover:text-blue-400">
            <a href="#contact">
              تماس با ما
            </a>
          </li>
        </ul>


        <!-- Button -->
        <a
            href="#contact"
            class="rounded-xl  px-5 py-3 transition"
        >

        </a>


      </nav>

    </div>
  </header>
</template>