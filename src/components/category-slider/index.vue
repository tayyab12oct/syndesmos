<template>
  <div class="flex flex-col space-y-2.5" :class="mainClass">
    <div class="flex items-center justify-center h-42" :class="imgMainClass">
      <img :src="src" alt="products" class="w-full h-full" />
    </div>
    <p
      class="text-gray-200 font-light text-center md:text-sm text-xs tracking-wide uppercase"
    >
      {{ title }}
    </p>
  </div>
</template>
<script setup lang="ts">
import { withDefaults, reactive } from "vue";

const props = withDefaults(
  defineProps<{
    mainClass?: string;
    imgMainClass?: string;
    imgClass?: string;
    src?: string;
    title?: string;
  }>(),
  { src: "/brands/img5.png", title: "PACK" }
);
</script>
