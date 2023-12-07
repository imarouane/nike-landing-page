<script setup>
import { services } from "@/constants";
import ServiceCard from "@/components/ServiceCard.vue";
</script>
<template>
  <div class="max-container flex flex-wrap justify-center gap-9" v-motion-slide-visible-once-bottom>
    <ServiceCard
      v-for="service in services"
      :key="service.label"
      :service="service"
    />
  </div>
</template>
