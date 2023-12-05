<script setup>
import { star } from "../assets/icons";
const props = defineProps({
  product: {
    type: Object,
    required: true,
  },
});
</script>

<template>
  <div class="flex w-full flex-1 flex-col max-sm:w-full">
    <img
      :src="product.imgURL"
      :alt="product.name"
      class="w-full"
    />
    <div class="mt-8 flex justify-start gap-2.5">
      <img :src="star" alt="rating" width="24" height="24" />
      <p class="font-montserrat text-xl leading-normal text-slate-gray">
        {{ product.rating }}
      </p>
    </div>
    <h3 class="mt-2 font-palanquin text-2xl font-semibold leading-normal">
      {{ product.name }}
    </h3>
    <p
      class="mt-2 font-montserrat text-2xl font-semibold leading-normal text-coral-red-600"
    >
      {{ product.price }}
    </p>
  </div>
</template>
