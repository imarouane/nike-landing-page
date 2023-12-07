<script setup>
import { ref } from "vue";
import AppButton from "@/components/AppButton.vue";
import ShoeCard from "@/components/ShoeCard.vue";
import { arrowRight } from "@/assets/icons";
import { statistics, shoes } from "../constants";
import { bigShoe2 } from "../assets/images";

let bigShoeHeroImg = ref(bigShoe2);
const changeHeroImg = (newBigShoeImg) => {
  bigShoeHeroImg.value = newBigShoeImg;
};
</script>
<template>
  <div
    class="max-container relative flex min-h-screen w-full flex-col justify-center gap-10 xl:flex-row"
  >
    <div
      class="max-xl:paddig-x padding-l relative flex w-full flex-col items-start justify-center pt-28 max-xl:pt-40 xl:w-2/5"
    >
      <p class="font-montserrat text-xl text-coral-red-600">
        Our Summer Collections
      </p>
      <h1
        class="font-palanquin text-8xl font-bold max-sm:text-[72px] max-sm:leading-[82px]"
      >
        <span class="relative z-10 block pr-10 xl:whitespace-nowrap xl:bg-white"
          >The New Arrival</span
        >
        <span class="mt-2 inline-block text-coral-red-600">Nike </span>
        Shoes
      </h1>
      <p
        class="mb-14 mt-6 font-montserrat text-lg leading-8 text-slate-gray sm:max-w-sm"
      >
        Discover stylish Nike arrivals, quality comfort, and innovation for your
        active life.
      </p>
      <AppButton label="Shop Now" :iconUrl="arrowRight" />
      <div
        class="mt-20 flex w-full flex-wrap items-start justify-start gap-10 gap-y-4 sm:gap-x-16"
      >
        <div v-for="statistic in statistics" :key="statistic.label">
          <p class="font-palanquin text-4xl font-bold">{{ statistic.value }}</p>
          <p class="font-montserrat leading-7 text-slate-gray">
            {{ statistic.label }}
          </p>
        </div>
      </div>
    </div>
    <div
      class="relative flex min-h-[80vh] flex-1 items-center justify-center bg-primary bg-hero bg-cover bg-center max-xl:py-40 xl:min-h-screen"
    >
      <div
        class="absolute overflow-hidden max-xl:pb-20"
        v-motion
        :initial="{ opacity: 0.5, x: 600 }"
        :enter="{
          opacity: 1,
          x: 0,
          transition: {
            duration: 500,
          },
        }"
      >
        <img
          :src="bigShoeHeroImg"
          alt="Shoe Collection"
          width="610"
          height="502"
          class="z-10 -rotate-[24deg] object-contain"
        />
      </div>
      <div class="absolute -bottom-[5%] flex gap-4 max-sm:px-6 sm:gap-6">
        <ShoeCard
          v-for="(shoe, index) in shoes"
          :key="index"
          :imgUrl="shoe"
          @changeBigImg="changeHeroImg"
          :selected="shoe.bigShoe === bigShoeHeroImg"
        />
      </div>
    </div>
  </div>
</template>
<style></style>
