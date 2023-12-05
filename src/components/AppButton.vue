<script setup>
const props = defineProps({
  label: {
    type: String,
    required: true,
    default: "Click me",
  },
  iconUrl: {
    type: String,
    required: false,
  },
  bgColor: {
    type: String,
  },
  borderColor: {
    type: String,
  },
  textColor: {
    type: String,
  },
});
</script>

<template>
  <button
    class="leading-non group flex items-center justify-center gap-2 rounded-full border px-7 py-4 font-montserrat text-lg"
    :class="[
      bgColor
        ? `${bgColor} ${borderColor} ${textColor}`
        : 'border-coral-red bg-coral-red text-white hover:bg-coral-red-500',
    ]"
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
