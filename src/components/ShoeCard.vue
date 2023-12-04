<script setup>
import { defineProps, defineEmits } from "vue";
let props = defineProps({
  imgUrl: {
    type: Object,
    required: true,
  },
  selected: {
    type: Boolean,
    default: false,
  },
});
const emit = defineEmits();
const selectShoe = () => {
  emit("changeBigImg", props.imgUrl.bigShoe);
};
</script>

<template>
  <div
    class="cursor-pointer rounded-xl border-2 max-sm:flex-1"
    :class="{ 'border-coral-red-600': selected }"
    @click="selectShoe"
  >
    <div
      class="flex items-center justify-center rounded-xl bg-card bg-cover bg-center max-sm:p-4 sm:h-40 sm:w-40"
    >
      <img
        :src="props.imgUrl.thumbnail"
        alt="Shoe Collection"
        width="150"
        height="126"
        class="-rotate-[12deg] object-contain"
      />
    </div>
  </div>
</template>
