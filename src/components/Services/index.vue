<template>
  <div
    class="grid md:grid-cols-4 grid-cols-1 md:divide-x divide-y md:divide-y-0 divide-gray-300 md:py-6 py-3 px-6 md:px-0 border border-gray-400"
  >
    <div
      class="text-center space-y-1 py-4 lg:px-8 px-3"
      v-for="v in 4"
      :key="v"
    >
      <p class="leading-4 text-2xs lg:text-base">Lorem ipsum dolor sit amet.</p>
      <p
        class="lg:text-sm text-2xs font-light text-gray-700 lg:leading-5 leading-[14px]"
      >
        Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet consectetur
      </p>
    </div>
  </div>
</template>
<script setup lang="ts">
import { withDefaults } from "vue";
const props = withDefaults(
  defineProps<{
    className?: string;
  }>(),
  {
    className: "",
  }
);
</script>
