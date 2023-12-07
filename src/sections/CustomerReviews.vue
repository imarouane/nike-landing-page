<script setup>
import { reviews } from "@/constants";
import ReviewCard from "@/components/ReviewCard.vue";
</script>

<template>
  <div class="max-conatiner">
    <div class="flex flex-col items-center gap-5">
      <h3 class="font-palanquin text-4xl font-bold">
        What Our <span class="text-coral-red-600">Customers</span> Say?
      </h3>
      <p class="info-text max-w-lg text-center">
        Hear genuine stories from our satisfied customers about their
        exceptional experiences with us.
      </p>
    </div>
    <div
      class="mt-24 flex flex-1 items-center justify-evenly gap-14 max-lg:flex-col"
      v-motion-slide-visible-once-bottom
    >
      <ReviewCard
        v-for="review in reviews"
        :key="review.customerName"
        :review="review"
      />
    </div>
  </div>
</template>
