<script setup>
import AppButton from "@/components/AppButton.vue";
import { shoe8 } from "../assets/images";
</script>
<template>
  <div
    class="max-container flex w-full items-center justify-between gap-10 max-lg:flex-col"
  >
    <div class="flex flex-1 flex-col">
      <h2 class="font-palanquin text-4xl font-bold capitalize lg:max-w-lg">
        We Provide You
        <span class="text-coral-red-600">Super </span>
        <span class="text-coral-red-600">Qulaity</span>
        Shoes
      </h2>
      <p class="info-text mt-4 lg:max-w-lg">
        Ensuring premium comfort and style, our meticulously crafted footwear is
        designed to elevate your experience, providing you with unmatched
        quality, innovation, and a touch of elegance.
      </p>
      <p class="mt-6 lg:max-w-lg">
        Our dedication to detail and excellence ensures your satisfaction
      </p>
      <div class="mt-11">
        <AppButton label="View Details" />
      </div>
    </div>
    <figure class="flex flex-1 items-center justify-center">
      <img
        :src="shoe8"
        alt="super quality shoe"
        width="570"
        height="522"
        class="object-contain"
      />
    </figure>
  </div>
</template>
