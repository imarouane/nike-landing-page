<script setup>
import { products } from "@/constants";
import PoplarProductCard from "@/components/PoplarProductCard.vue";
</script>
<template>
  <div class="max-container">
    <div class="flex flex-col justify-start gap-5">
      <h2 class="font-palanquin text-4xl font-bold">
        Our <span class="text-coral-red-600">Popular</span> Products
      </h2>
      <p class="text-justify font-montserrat text-slate-gray lg:max-w-2xl">
        Explore the latest popular Nike Shoes, seamlessly blending style and
        performance. From timeless classics to cutting-edge designs, each step
        is a statement.
      </p>
    </div>
    <div
      class="mt-16 grid grid-cols-1 gap-14 sm:grid-cols-2 sm:gap-4 md:grid-cols-3 lg:grid-cols-4"
      v-motion-slide-visible-once-bottom
    >
      <PoplarProductCard
        v-for="product in products"
        :key="product.name"
        :product="product"
      />
    </div>
  </div>
</template>

<style></style>
