<script setup>
const props = defineProps({
  label: {
    type: String,
    required: true,
    default: "Click me",
  },
  iconUrl: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <button
    class="group flex items-center justify-center gap-2 rounded-full border border-coral-red bg-coral-red px-7 py-4 font-montserrat text-lg leading-none text-white hover:bg-coral-red-500"
  >
    {{ props.label }}
    <img
      v-if="iconUrl"
      :src="props.iconUrl"
      alt="Icon"
      class="h-5 w-5 rounded-full transition duration-200 ease-out group-hover:translate-x-1"
    />
  </button>
</template>
