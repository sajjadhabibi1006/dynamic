<template>
  <section class="relative h-screen overflow-hidden">

    <!-- Background -->
    <div class="absolute inset-0">

      <img
          :src="slides[current].image"
          :alt="slides[current].title"
          class="w-full h-full object-cover"
      />


      <!-- Dark layer -->
      <div
          class="
        absolute inset-0
  bg-gradient-to-l
from-[#020617]/90
via-[#020617]/40
to-transparent
        "
      ></div>

    </div>


    <!-- Content -->
    <div
        class="
      relative z-10
      h-full
      flex
      items-center
      "
    >

      <div
          class="
        container
        mx-auto
        px-8
        "
      >

        <div
            class="
  max-w-xl
  ml-auto
  text-right
  "
        >


          <!-- Small title -->
          <span
              class="
            inline-block
            mb-6
            px-5
            py-2
            rounded-full
            bg-blue-500/20
            text-blue-400
            text-sm
            "
          >
            {{ slides[current].subtitle }}
          </span>


          <!-- Main title -->
          <h1
              class="
text-white
text-3xl
md:text-5xl
font-bold
leading-[1.6]
"
          >

            {{ slides[current].title }}

            <span class="text-blue-500">
              {{ slides[current].highlight }}
            </span>

          </h1>



          <!-- Description -->
          <p
              class="
            mt-6
            text-gray-300
            text-base
            leading-9
            max-w-xl
            "
          >
            {{ slides[current].description }}
          </p>



          <!-- Buttons -->
          <div
              class="
            mt-8
            flex
            justify-end
            gap-4
            "
          >

            <a
                href="contact-us"
                class="
              bg-blue-600
              hover:bg-blue-700
              px-8
              py-4
              rounded-xl
              text-white
              transition
              shadow-[0_0_30px_rgba(37,99,235,.5)]
              "
            >
              تماس با ما
            </a>


            <a
                href="#services"
                class="
              border
              border-white/20
              hover:bg-white/10
              px-8
              py-4
              rounded-xl
              text-white
              transition
              "
            >
              خدمات ما
            </a>


          </div>


        </div>


      </div>

    </div>



    <!-- Scroll -->
    <div
        class="
      absolute
      bottom-8
      left-1/2
      -translate-x-1/2
      text-white
      text-3xl
      "
    >
      ↓
    </div>


  </section>
</template>



<script setup>

const current = ref(0)


const slides = [
  {
    image:'/images/slide1.png',

    subtitle:'راهکارهای تخصصی صنعتی',

    title:'مهندسی تعمیرات صنعتی',

    highlight:' دینامیک',

    description:
        'ارائه خدمات تخصصی، تعمیرات و پشتیبانی با تیمی مجرب و تجهیزات پیشرفته.'
  }
]


</script>