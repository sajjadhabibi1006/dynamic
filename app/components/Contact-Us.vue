<template>
  <section
    id="contact-us"
    dir="rtl"
    class="relative overflow-hidden py-24"
  >
    <!-- Background Glow -->
    <div
      class="pointer-events-none absolute -top-32 right-1/4
      h-96 w-96 rounded-full
      bg-cyan-500/10 blur-3xl"
    ></div>

    <div
      class="pointer-events-none absolute -bottom-32 left-1/4
      h-96 w-96 rounded-full
      bg-blue-500/10 blur-3xl"
    ></div>


    <div class="container relative mx-auto px-6">

      <!-- Header -->
      <div class="mx-auto mb-14 max-w-2xl text-center">

        <span
          class="mb-4 inline-flex items-center rounded-full
          border border-white/10 bg-white/5
          px-4 py-2 text-sm text-gray-300
          backdrop-blur-xl"
        >
          تماس با ما
        </span>

        <p
          class="text-base leading-8 text-white-400 md:text-lg"
        >
         کلیه خدمات عیب‌یابی، سرویس و تعمیرات سنگین در محل کارگاه،
         کارخانه یا پروژه مشتری انجام می‌پذیرد.
         جهت ثبت درخواست اعزام فوری کارشناس با شماره مستقیم پشتیبانی تماس حاصل فرمایید.
        </p>


<!-- 
        <h2
          class="mb-5 text-3xl font-black tracking-tight
          text-white md:text-5xl"
        >
          با ما در ارتباط باشید
        </h2> -->

        <br>

        <p
          class="text-base leading-8 text-gray-300 md:text-lg"
        >
          از طریق شبکه‌های اجتماعی زیر می‌توانید با ما
          در ارتباط باشید و پاسخ سوالات خود را دریافت کنید.
        </p>

        <br><br>
        
        <h2
          class="mb-5 text-3xl font-black tracking-tight
          text-white md:text-5xl"
        >
          با ما در ارتباط باشید.
        </h2>

        

      </div>


      <!-- Cards -->
      <div
        class="grid gap-6 sm:grid-cols-2 lg:grid-cols-4"
      >

        <a
          v-for="item in contacts"
          :key="item.title"
          :href="item.url"
          target="_blank"
          rel="noopener noreferrer"
          :aria-label="`ارتباط با ما در ${item.title}`"
          class="contact-card group relative overflow-hidden
          rounded-3xl border border-white/10
          bg-white/[0.04] p-7
          backdrop-blur-xl
          transition-all duration-500
          hover:-translate-y-3
          hover:border-white/20
          hover:bg-white/[0.08]"
          :class="item.hoverClass"
        >

          <!-- Card Glow -->
          <div
            class="absolute -right-10 -top-10
            h-32 w-32 rounded-full
            opacity-0 blur-3xl
            transition duration-500
            group-hover:opacity-100"
            :class="item.glowClass"
          ></div>


          <!-- Icon -->
          <div
            class="relative mb-7 flex h-16 w-16
            items-center justify-center
            rounded-2xl border border-white/10
            bg-white/5
            shadow-xl
            transition-all duration-500
            group-hover:scale-110
            group-hover:rotate-3"
            :class="item.iconContainerClass"
          >

            <!-- Rainbow Glow فقط برای روبیکا -->
            <div
              v-if="item.type === 'rubika'"
              class="pointer-events-none absolute
              inset-0 rounded-2xl opacity-0
              blur-md transition-opacity duration-500
              group-hover:opacity-100
              bg-[linear-gradient(45deg,#ef4444,#f97316,#eab308,#22c55e,#06b6d4,#3b82f6,#a855f7,#ec4899)]"
            ></div>


            <!-- Icon Image -->
            <img
              :src="item.icon"
              :alt="item.title"
              class="relative z-10
              h-9 w-9
              object-contain
              transition-all duration-500"
              :class="item.iconClass"
            />

          </div>


          <!-- Content -->
          <div class="relative">

            <h3
              class="mb-3 text-xl font-bold text-white"
            >
              {{ item.title }}
            </h3>

            <p
              class="min-h-[56px]
              text-sm leading-7
              text-gray-400"
            >
              {{ item.text }}
            </p>

          </div>


          <!-- CTA -->
          <div
            class="relative mt-7 flex items-center
            justify-between
            border-t border-white/10
            pt-5"
          >

            <span
              class="text-sm font-medium
              text-gray-400
              transition
              group-hover:text-white"
            >
              ورود به {{ item.title }}
            </span>

            <span
              class="flex h-9 w-9
              items-center justify-center
              rounded-full
              border border-white/10
              bg-white/5
              text-gray-400
              transition-all duration-300
              group-hover:-translate-x-1
              group-hover:text-white"
            >
              ←
            </span>

          </div>

        </a>

      </div>

    </div>
  </section>
</template>


<script setup>

const contacts = [

  {
    type: 'telegram',

    title: 'تلگرام',

    text:
      'برای دریافت اطلاعات و پشتیبانی از طریق تلگرام با ما در ارتباط باشید.',

    url:
      'https://t.me/MostafaGhasemi1371',

    icon:
      '/social-icons/telegram.svg',

    hoverClass:
      'hover:shadow-[0_20px_60px_rgba(34,158,217,0.20)]',

    glowClass:
      'bg-sky-500',

    iconContainerClass:
      'group-hover:border-sky-400/30',

    iconClass:
      'group-hover:scale-110'

  },


  {
    type: 'whatsapp',

    title: 'واتساپ',

    text:
      'برای ارتباط مستقیم و سریع، از طریق واتساپ با ما تماس بگیرید.',

    url:
      'https://wa.me/MostafaGhasemi1371',

    icon:
      '/social-icons/whatsapp.svg',

    hoverClass:
      'hover:shadow-[0_20px_60px_rgba(37,211,102,0.20)]',

    glowClass:
      'bg-green-500',

    iconContainerClass:
      'group-hover:border-green-400/30',

    iconClass:
      'group-hover:scale-110'

  },


  {
    type: 'rubika',

    title: 'روبیکا',

    text:
      'برای ارتباط با مجموعه ما می‌توانید از پیام‌رسان روبیکا استفاده کنید.',

    url:
      'https://rubika.ir/MostafaGhasemi1371',

    icon:
      '/social-icons/rubika.svg',

    hoverClass:
      'hover:shadow-[0_20px_60px_rgba(168,85,247,0.25)]',

    glowClass:
      'bg-violet-500',

    iconContainerClass:
      'group-hover:border-transparent',

    iconClass:
      'group-hover:scale-110'

  },


  {
    type: 'eitaa',

    title: 'ایتا',

    text:
      'از طریق پیام‌رسان ایتا نیز می‌توانید با ما در ارتباط باشید.',

    url:
      'https://eitaa.com/MostafaGhasemi1371',

    icon:
      'https://eitaa.com/img/eitaa_logo.svg',

    hoverClass:
      'hover:shadow-[0_20px_60px_rgba(249,115,22,0.25)]',

    glowClass:
      'bg-orange-500',

    iconContainerClass:
      'group-hover:border-orange-400/30',

    iconClass:
      'group-hover:scale-110'

  }

]

</script>

