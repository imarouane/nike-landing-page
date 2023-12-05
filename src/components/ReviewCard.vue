<script setup>
import { star } from "@/assets/icons";

const props = defineProps({
  review: {
    type: Object,
    required: true,
  },
});
</script>

<template>
  <div class="flex flex-col items-center justify-center">
    <img
      :src="review.imgURL"
      alt="customer review"
      class="h-[120px] w-[120px] rounded-full object-cover"
    />
    <p class="info-text mt-6 max-w-sm text-center">{{ review.feedback }}</p>
    <div class="mt-3 flex items-center justify-center gap-2.5">
      <img
        :src="star"
        alt="star icon"
        width="24"
        height="24"
        class="m-0 object-contain"
      />
      <p class="font-montserrat text-xl text-slate-gray">
        ({{ review.rating }})
      </p>
    </div>
    <h2 class="mt-1 text-center font-palanquin text-3xl font-bold">
      {{ review.customerName }}
    </h2>
  </div>
</template>
