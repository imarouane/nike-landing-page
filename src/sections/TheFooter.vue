<script setup>
import { footerLogo } from "@/assets/images";
import { socialMedia, footerLinks } from "@/constants";
import { copyrightSign } from "@/assets/icons";
</script>
<template>
  <div class="max-container">
    <div
      class="flex flex-wrap items-start justify-between gap-20 max-lg:flex-col"
    >
      <div class="flex flex-col items-start">
        <a href="/">
          <img
            :src="footerLogo"
            alt="Nike"
            width="150"
            height="46"
            class="m-0"
          />
        </a>
        <p
          class="mt-5 font-montserrat text-base leading-7 text-white-400 sm:max-w-sm"
        >
          Get shoes ready for the new term at your nearest Nike store. Find Your
          perfect Size In Store. Get Rewards
        </p>
        <div class="mt-8 flex items-center gap-5">
          <div
            v-for="icon in socialMedia"
            :key="icon.alt"
            class="flex h-12 w-12 items-center justify-center rounded-full bg-white"
          >
            <img :src="icon.src" :alt="icon.alt" />
          </div>
        </div>
      </div>
      <div
        class="flex flex-1 justify-between gap-20 max-lg:flex-wrap lg:gap-10"
      >
        <div v-for="section in footerLinks" :key="section.title">
          <h4
            class="mb-6 font-montserrat text-2xl font-medium leading-normal text-white"
          >
            {{ section.title }}
          </h4>
          <ul>
            <li
              v-for="link in section.links"
              :key="link.name"
              class="mt-3 font-montserrat text-base leading-normal text-white-400 hover:text-slate-200"
            >
              <a :href="link.link">{{ link.name }}</a>
            </li>
          </ul>
        </div>
      </div>
    </div>
    <div
      class="mt-24 flex justify-between text-white-400 max-sm:flex-col max-sm:items-center"
    >
      <div
        class="flex flex-1 cursor-pointer items-center gap-2 font-montserrat"
      >
        <img
          :src="copyrightSign"
          alt="copyright"
          width="20"
          height="20"
          class="m-0 rounded-full"
        />
        <p>Copyright. All rights reserved.</p>
      </div>
      <p class="cursor-pointer font-montserrat">Terms & Conditions</p>
    </div>
  </div>
</template>
