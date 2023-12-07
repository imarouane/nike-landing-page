<script setup>
import AppButton from "@/components/AppButton.vue";
import { arrowRight } from "../assets/icons";
import { offer } from "@/assets/images";
</script>

<template>
  <div
    class="max-conatiner flex w-full items-center justify-between gap-10 max-lg:flex-col-reverse"
  >
    <figure class="flex-1" v-motion-slide-visible-once-left>
      <img
        :src="offer"
        alt="super quality shoe"
        width="773"
        height="687"
        class="object-contain"
      />
    </figure>
    <div class="flex flex-1 flex-col" v-motion-slide-visible-once-right>
      <h2 class="font-palanquin text-4xl font-bold capitalize lg:max-w-lg">
        <span class="text-coral-red-600">Special </span>
        Offer
      </h2>
      <p class="info-text mt-4">
        Embark on a shopping journey that redefines your experience with
        unbeatable deals. From premier selections to incredible savings, we
        offer unparalleled value that sets us apart.
      </p>
      <p class="info-text mt-6">
        Navigate a realm of possibilities designed to fulfill your unique
        desires, surpassing the loftiest expectations. Your journey with us is
        nothing short of exceptional.
      </p>
      <div class="mt-11 flex flex-wrap gap-4">
        <AppButton label="Shop Now" :iconUrl="arrowRight" />
        <AppButton
          label="Learn More"
          borderColor="border-slate-gray"
          bgColor="bg-white"
          textColor="text-slate-gray"
        />
      </div>
    </div>
  </div>
</template>
