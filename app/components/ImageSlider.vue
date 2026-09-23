<script setup>
import { ref, computed, onMounted, onBeforeUnmount } from 'vue'

const props = defineProps({
  images: {
    type: Array,
    default: () => []
  }
})

const currentIndex = ref(0)
const screenWidth = ref(1200)

const updateWidth = () => {
  screenWidth.value = window.innerWidth
}

onMounted(() => {
  updateWidth()
  window.addEventListener('resize', updateWidth)
})

onBeforeUnmount(() => {
  window.removeEventListener('resize', updateWidth)
})

const visibleCount = computed(() => {
  if (screenWidth.value < 640) return 1
  if (screenWidth.value < 1024) return 2
  if (screenWidth.value < 1280) return 3
  return 4
})

const maxIndex = computed(() => {
  return Math.max(0, props.images.length - visibleCount.value)
})

const canNext = computed(() => {
  return currentIndex.value < maxIndex.value
})

const canPrev = computed(() => {
  return currentIndex.value > 0
})

const next = () => {
  if (canNext.value) {
    currentIndex.value++
  }
}

const prev = () => {
  if (canPrev.value) {
    currentIndex.value--
  }
}

const slideStyle = computed(() => ({
  width: `${100 / visibleCount.value}%`,
  flex: `0 0 ${100 / visibleCount.value}%`
}))

const trackStyle = computed(() => ({
  transform: `translateX(-${currentIndex.value * (100 / visibleCount.value)}%)`
}))
</script>

<template>
  <div
    class="image-slider"
    dir="ltr"
  >
    <div
      class="image-slider-window"
    >
      <div
        class="image-slider-track"
        :style="trackStyle"
      >
        <div
          v-for="(image, index) in images"
          :key="index"
          class="image-slider-item"
          :style="slideStyle"
        >
          <img
            :src="image.src"
            :alt="image.alt || `تصویر ${index + 1}`"
            class="image-slider-image"
          >
        </div>
      </div>
    </div>

    <!-- قبلی -->
    <button
      v-if="canPrev"
      type="button"
      class="slider-arrow slider-prev"
      @click="prev"
    >
      ‹
    </button>

    <!-- بعدی -->
    <button
      v-if="canNext"
      type="button"
      class="slider-arrow slider-next"
      @click="next"
    >
      ›
    </button>
  </div>
</template>

<style scoped>
.image-slider {
  position: relative;
  width: 100%;
  max-width: 100%;
}

.image-slider-window {
  width: 100%;
  overflow: hidden;
}

.image-slider-track {
  display: flex;
  width: max-content;
  transition: transform 0.5s ease;
}

.image-slider-item {
  box-sizing: border-box;
  padding: 0 8px;
  min-width: 0;
}

.image-slider-image {
  display: block;
  width: 100%;
  height: 240px;
  object-fit: cover;
  border-radius: 16px;
}

.slider-arrow {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  z-index: 10;

  width: 42px;
  height: 42px;

  border: 0;
  border-radius: 50%;

  background: rgba(0, 0, 0, 0.7);
  color: white;

  font-size: 32px;
  line-height: 1;

  cursor: pointer;

  display: flex;
  align-items: center;
  justify-content: center;
}

.slider-arrow:hover {
  background: rgba(0, 0, 0, 0.9);
}

.slider-prev {
  left: 10px;
}

.slider-next {
  right: 10px;
}

/* موبایل */
@media (max-width: 639px) {
  .image-slider-image {
    height: 220px;
  }
}

/* تبلت */
@media (min-width: 640px) and (max-width: 1023px) {
  .image-slider-image {
    height: 230px;
  }
}
</style>