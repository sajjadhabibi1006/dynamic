<script setup lang="ts">
</script>
<template>
  <header
      class="fixed top-0 w-full z-50 bg-black/20 backdrop-blur-md relative"
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
      
<div class="flex items-center gap-2" dir="rtl">

  <!-- Logo -->
  <div class="relative w-14 h-14 shrink-0">
    <a href="/">
    <img
      src="/images/logo.png"
      alt="دینامیک"
      class="absolute w-20 h-30 max-w-none object-contain top-1/2 right-0 -translate-y-1/2"
    >
    </a>
  </div>

  <!-- Text -->
  <div class="flex flex-col leading-tight text-right whitespace-nowrap">
    <h1 class="text-base font-bold text-white mr-5">
      دینامیک
    </h1>

    <span class="text-xs text-gray-400 mt-1 mr-5">
      تعمیرات صنعتی
    </span>
  </div>

</div>
 <MobileMenu />

        <!-- Menu -->
        <ul
            class="hidden md:flex items-center gap-8 text-gray-300"
        >
          <li class="hover:text-blue-400">
            <a href="/">
              صفحه اصلی
            </a>
          </li>

          <li class="hover:text-blue-400">
            <a href="diesel">
              دیزل و ژنراتور
            </a>
          </li>

          <li class="hover:text-blue-400">
            <a href="qutein">
             پِرس و گیوتین 
            </a>
          </li>

          <li class="hover:text-blue-400">
            <a href="mechanical-systems">
            تاسیسات مکانیکی
            </a>
          </li>

          <li class="hover:text-blue-400">
            <a href="construction-machinery">
             ماشین آلات ساختمانی
            </a>
          </li>

            <li class="hover:text-blue-400">
            <a href="agricultural-machinery">
             ماشین آلات کشاورزی
            </a>
          </li>

          <li class="hover:text-blue-400">
            <a href="about-us">
              درباره ما
            </a>
          </li>

          <li class="hover:text-blue-400">
            <a href="contact-us">
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