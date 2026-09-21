<template>
  <section
      id="services"
      class="py-24"
  >
    <div class="container mx-auto px-6">

      <div class="text-center mb-12">

        <h2
            class="text-3xl md:text-5xl font-black mb-4"
        >
          خدمات ما
        </h2>

        <p class="text-gray-400">
          ارائه راهکارهای تخصصی با کیفیت بالا
        </p>

      </div>


      <div
          class="grid md:grid-cols-3 gap-6"
      >

        <div
            v-for="item in services"
            :key="item.title"
            class="rounded-3xl border border-white/10
          bg-white/5 backdrop-blur-xl
          p-8 hover:-translate-y-2
          transition"
        >

          <div
              class="text-4xl mb-5"
          >
            {{ item.icon }}
          </div>


          <h3
              class="text-xl font-bold mb-3"
          >
            {{ item.title }}
          </h3>


          <p
              class="text-gray-400 leading-7"
          >
            {{ item.text }}
          </p>


        </div>

      </div>

    </div>
  </section>
</template>


<script setup>

const services = [
  {
    icon: '⚙️',
    title: 'تعمیرات تخصصی',
    text: 'ارائه خدمات تعمیر و نگهداری تجهیزات صنعتی'
  },

  {
    icon: '🏭',
    title: 'مشاوره صنعتی',
    text: 'بررسی و ارائه بهترین راهکار برای پروژه‌ها'
  },

  {
    icon: '🛠️',
    title: 'پشتیبانی فنی',
    text: 'همراهی و پشتیبانی پس از انجام خدمات'
  }
]

</script>