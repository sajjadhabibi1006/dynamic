<script setup>
import { ref } from 'vue'

const isMenuOpen = ref(false)
</script>

<template>
  <div class="relative ml-auto md:hidden">

    <!-- دکمه همبرگری -->
    <button
      @click="isMenuOpen = !isMenuOpen"
      class="flex flex-col justify-center items-center gap-1.5 w-10 h-10"
      aria-label="باز کردن منو"
    >
      <span
        class="w-7 h-0.5 bg-white transition-all duration-300"
        :class="isMenuOpen ? 'rotate-45 translate-y-2' : ''"
      ></span>

      <span
        class="w-7 h-0.5 bg-white transition-all duration-300"
        :class="isMenuOpen ? 'opacity-0' : ''"
      ></span>

      <span
        class="w-7 h-0.5 bg-white transition-all duration-300"
        :class="isMenuOpen ? '-rotate-45 -translate-y-2' : ''"
      ></span>
    </button>

    <!-- منو -->
    <Transition
      enter-active-class="transition duration-300"
      enter-from-class="opacity-0 -translate-y-4"
      enter-to-class="opacity-100 translate-y-0"
      leave-active-class="transition duration-300"
      leave-from-class="opacity-100 translate-y-0"
      leave-to-class="opacity-0 -translate-y-4"
    >
      <div
        v-if="isMenuOpen"
        class="absolute top-full left-0 w-64 bg-slate-900 z-[999] p-6 border-t border-white/10"
      >
        <ul class="flex flex-col gap-5 text-right text-white">

          <li>
            <NuxtLink to="/" @click="isMenuOpen = false">
              صفحه اصلی
            </NuxtLink>
          </li>

          <li>
            <NuxtLink to="/about" @click="isMenuOpen = false">
              درباره ما
            </NuxtLink>
          </li>

          <li>
            <NuxtLink to="/diesel-generator" @click="isMenuOpen = false">
              دیزل ژنراتور
            </NuxtLink>
          </li>

          <li>
            <NuxtLink to="/construction-machinery" @click="isMenuOpen = false">
              ماشین آلات ساختمانی
            </NuxtLink>
          </li>

          <li>
            <NuxtLink to="/mechanical-facilities" @click="isMenuOpen = false">
              تأسیسات مکانیکی
            </NuxtLink>
          </li>

          <li>
            <NuxtLink to="/contact" @click="isMenuOpen = false">
              تماس با ما
            </NuxtLink>
          </li>

        </ul>
      </div>
    </Transition>

  </div>
</template>