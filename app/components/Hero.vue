<template>
  <section
      class="relative min-h-screen pt-32 overflow-hidden flex items-center"
  >
    <!-- Background Glow -->
    <div
        class="absolute top-20 right-20 w-72 h-72 bg-blue-600/30 blur-[120px] rounded-full"
    ></div>

    <div
        class="container mx-auto px-6 relative z-10"
    >

      <div
          class="grid lg:grid-cols-2 gap-12 items-center"
      >

        <!-- Text -->
        <div class="text-right">

          <span
              class="inline-block mb-5 px-4 py-2 rounded-full bg-blue-500/10 text-gray-100 text-sm"
          >
            راهکارهای تخصصی صنعتی
          </span>


          <h1
              class="text-4xl md:text-6xl font-black leading-tight mb-6"
          >
            خدمات حرفه‌ای
            <span class="text-blue-500">
              صنعتی
            </span>
            با استاندارد جهانی
          </h1>


          <p
              class="text-gray-400 text-lg leading-8 mb-8 max-w-xl"
          >
            ارائه خدمات تخصصی، تعمیرات و پشتیبانی
            با تیمی مجرب و تجهیزات پیشرفته.
          </p>


          <div class="flex gap-4 justify-start">

            <a
                href="contact-us"
                class="bg-blue-600 hover:bg-blue-700 transition px-8 py-4 rounded-xl"
            >
              تماس با ما
            </a>


            <a
                href="#"
                class="border border-white/20 hover:bg-white/10 transition px-8 py-4 rounded-xl"
            >
              خدمات ما
            </a>

          </div>

        </div>



        <!-- Image -->
        <div
            class="relative"
        >

          <div
              class="absolute inset-0 bg-blue-500/20 blur-3xl rounded-full"
          ></div>


          <img
              src="/images/slide1.png"
              alt="Industrial"
              class="relative z-10 rounded-3xl shadow-2xl"
          />

        </div>


      </div>

    </div>

  </section>
</template>