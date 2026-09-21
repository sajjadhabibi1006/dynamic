<script setup lang="ts">
import Diesel from "~/pages/diesel.vue";
</script>
<template>
  <div>

    <Header />

    <main>

      <diesel/>
      <section>
        <!-- همان کدهای اسلایدی که نوشتی -->
      </section>


      <!-- بخش دپارتمان -->
      <DieselDepartment />


    </main>

    <NuxtPage />

    <Footer />

  </div>
</template>