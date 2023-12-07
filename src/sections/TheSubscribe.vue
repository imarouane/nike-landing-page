<script setup>
import AppButton from "../components/AppButton.vue";
</script>
<template>
  <div
    class="max-container flex items-center justify-between gap-10 max-lg:flex-col"
  >
    <h3
      class="font-palanquin text-4xl font-bold leading-[68px] lg:max-w-lg"
      v-motion-slide-visible-once-left
    >
      Sign Up from
      <span class="text-coral-red-600">Updates </span>
      & Newsletter
    </h3>

    <div class="w-full lg:max-w-[40%]" v-motion-slide-visible-once-right>
      <form
        class="flex items-center justify-center gap-2 max-sm:flex-wrap max-sm:gap-4 sm:rounded-full sm:border sm:border-slate-gray sm:px-3 sm:py-2.5"
      >
        <input
          type="email"
          name="email"
          placeholder="subscribe@nike.com"
          class="input"
        />
        <AppButton label="Sign Up" class="max-sm:flex-1" />
      </form>
    </div>
  </div>
</template>
