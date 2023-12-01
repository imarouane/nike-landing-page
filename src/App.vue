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
  <div>
    <TheNav />
    <main class="relative">
      <section class="xl:padding wide:padding-r padding-b">
        <TheHero />
      </section>
    </main>
  </div>
</template>
