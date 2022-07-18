<template>
  <div class="border">
    <div class="flex items-center justify-center border-b border-gray-700">
      <img src="/products/anti_hair.png" alt="products" />
    </div>
    <p class="text-center text-gray-600 font-light md:text-lg text-base pt-6">
      {{ title }}
    </p>
    <p class="text-center text-gray-600 font-light md:text-lg text-base pt-6">
      {{ desc }}
    </p>
    <p class="text-center text-gray-600 font-light md:text-lg text-base pt-6">
      {{ subtitle }}
    </p>
  </div>
</template>
<script setup>
import { reactive } from "vue";

const products = reactive([
  {
    src: "/products/anti_hair.png",
    title: "Woman's Placement Thinstrap",
    desc: "Muscleback Swimmsuit Blue/Black",
    subtitle: "Lorem ipsum dolor sit",
  },
]);
</script>
