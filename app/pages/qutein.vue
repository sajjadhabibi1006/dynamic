<template>
  <section
      class="
    relative
    h-screen
    overflow-hidden
    "
  >

    <!-- Background -->
    <div class="absolute inset-0">

<img
  src="/images/qutien/slide-qutein.png"
  alt="Diesel Generator"
  class="w-full 
  h-full 
  object-cover"
/>


      <!-- Dark Overlay -->
      <div
          class="
        absolute
        inset-0
        bg-gradient-to-l
        from-[#020617]/95
        via-[#020617]/70
        to-[#020617]/30
        "
      ></div>

    </div>



    <!-- Content -->

    <div
        class="
      relative
      z-10
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


        <!-- متن سمت راست -->

        <div
          class="
          max-w-xl
          ml-auto
          text-right
          "
        >


          <span
              class="
            inline-block
            mb-5
            px-5
            py-2
            rounded-full
            bg-blue-500/10
            text-blue-400
            text-sm
            "
          >
            تجهیزات و خدمات صنعتی
          </span>



          <h1
              class="
            text-white
            text-4xl
            md:text-5xl
            font-black
            leading-[1.5]
            "
          >

           ماشین‌آلات فرمینگ، 

            <span
                class="text-blue-500"
            >
             پرس، نورد و گیوتین
            </span>

          </h1>



          <p
              class="
            text-gray-300
            mt-6
            text-base
            md:text-lg
            leading-9
            "
          >

 خدمات تعمیرات و تنظیمات دقیق پرس‌های صنعتی و قیچی‌های برش

          </p>



          <div
              class="
            mt-8
            flex
            gap-4
            justify-end
            "
          >

            <a
                href="#contact"
                class="
              bg-blue-600
              hover:bg-blue-700
              transition
              text-white
              px-8
              py-4
              rounded-xl
              "
            >
              درخواست مشاوره
            </a>



            <a
                href="#services"
                class="
              border
              border-white/20
              hover:bg-white/10
              transition
              text-white
              px-8
              py-4
              rounded-xl
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
      text-2xl
      "
    >
      ↓
    </div>

  </section>

  <QuteinDepartment />

</template>