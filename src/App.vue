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
    <section id="home" class="padding-b">
      <TheHero />
    </section>
    <section
      id="products"
      class="padding max-sm:mt-12"
    >
      <PopularProducts />
    </section>
    <section id="about-us" class="padding">
      <SuperQuality />
    </section>
  </main>
</template>
