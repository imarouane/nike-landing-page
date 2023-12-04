<script setup>
import {
  TheHero,
  PopularProducts,
  SuperQuality,
  TheServices,
  SpecialOffer,
  CustomerReviews,
  TheSubscriber,
  TheFooter,
} from "@/sections";

import TheNav from "@/components/TheNav.vue";
</script>

<template>
  <main class="relative">
    <TheNav />
    <section
      id="home"
      class="xl:padding-l wide:padding-r padding-b"
    >
      <TheHero />
    </section>
    <section class="">

    </section>
  </main>
</template>
