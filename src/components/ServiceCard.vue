<script setup>
const props = defineProps({
  service: {
    type: Object,
    required: true,
  },
});
</script>

<template>
  <div
    class="w-full flex-1 rounded-[20px] px-10 py-16 shadow-3xl sm:w-[350px] sm:max-w-[350px]"
  >
    <div
      class="flex h-11 w-11 items-center justify-center rounded-full bg-coral-red-600"
    >
      <img :src="service.imgURL" width="24" height="24" :alt="service.label" />
    </div>
    <h3 class="mt-5 font-palanquin text-3xl font-bold leading-normal">
      {{ service.label }}
    </h3>
    <p class="mt-3 break-words font-montserrat text-lg text-slate-gray">
      {{ service.subtext }}
    </p>
  </div>
</template>
