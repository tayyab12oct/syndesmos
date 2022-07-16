<template>
  <div
    class="bg-primary text-white lg:text-2xs text-3xs py-1.5 font-light md:grid grid-cols-3 px-4 hidden"
  >
    <div></div>
    <div class="flex items-center justify-center lg:space-x-5 space-x-2">
      <router-link to="/" v-for="v in 4" :key="v">TopBar</router-link>
    </div>
    <div class="flex items-center justify-end space-x-1">
      <span>Lorem ipsum dolor sit amet consectetur.</span>
      <PhoneIcon class="lg:w-3 w-2.5" />
    </div>
  </div>
</template>
<script setup>
import { PhoneIcon } from "@heroicons/vue/outline";
</script>
