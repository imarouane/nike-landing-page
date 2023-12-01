<script setup>
import { headerLogo } from "@/assets/images";
import { hamburger } from "@/assets/icons";
import { navLinks } from "@/constants";
</script>
<template>
  <header class="padding-x py-8 absolute z-10 w-full">
    <nav class="flex justify-between items-center gap-2 max-container">
      <a href="/"
        ><img :src="headerLogo" alt="Nike Logo" width="130" height="29"
      /></a>
      <div class="flex-1 flex justify-center items-center max-lg:hidden max-lg:flex-col">
        <ul class="flex justify-center items-center grow gap-16">
          <li v-for="link in navLinks" :key="link.label">
            <a
              :href="link.href"
              class="font-montserrat leading-normal text-lg text-slate-gray hover:text-coral-red font-normal transition ease-in-out duration-200"
              >{{ link.label }}</a
            >
          </li>
        </ul>
        <div
          class="flex justify-end items-center gap-1 text-lg text-slate-700 font-montserrat font-semibold"
        >
          <a href="#">Sign In</a>
          <span>/</span>
          <a href="#">Explore now</a>
        </div>
      </div>
      <div class="hidden max-lg:block">
        <img width="25" height="25" :src="hamburger" alt="icon">
      </div>
    </nav>
  </header>
</template>
