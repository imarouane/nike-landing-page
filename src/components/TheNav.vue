<script setup>
import { ref } from "vue";
import { headerLogo } from "@/assets/images";
import { hamburger, xHide } from "@/assets/icons";
import { navLinks } from "@/constants";

let isMenuOpen = ref(false);
const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};
</script>
<template>
  <header class="padding-x py-8 absolute z-10 w-full">
    <nav class="flex justify-between items-center gap-2 max-container">
      <a href="/"
        ><img :src="headerLogo" alt="Nike Logo" width="130" height="30"
      /></a>
      <div
        class="flex-1 flex justify-center items-center gap-10 responsive-menu"
        :class="{ 'max-lg:hidden': !isMenuOpen }"
      >
        <ul
          class="flex justify-center items-center grow gap-12 max-lg:gap-8 max-lg:flex-col"
        >
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
          <a href="#" class="hover:text-slate-500 trabsition duration-200 ease-in-out">Sign In</a>
          <span>/</span>
          <a href="#" class="hover:text-slate-500 trabsition duration-200 ease-in-out">Explore now</a>
        </div>
      </div>
      <div
        class="hidden max-lg:block cursor-pointer"
        id="nav-hamburger"
        @click="toggleMenu"
      >
        <div v-if="!isMenuOpen">
          <img width="30" height="30" :src="hamburger" alt="icon" />
        </div>
        <div v-if="isMenuOpen">
          <img width="30" height="30" :src="xHide" alt="icon" />
        </div>
      </div>
    </nav>
  </header>
</template>
