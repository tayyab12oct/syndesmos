<template>
  <div class="group" :class="mainClass">
    <div>
      <div class="flex items-center justify-center" :class="imgMainClass">
        <img :src="src" alt="products" :class="imgClass" />
      </div>
    </div>
    <div class="px-3 py-2 space-y-1">
      <p class="text-gray-200 font-medium md:text-sm text-xs tracking-wide">
        {{ title }}
      </p>
      <p
        class="text-gray-600 font-light md:text-xs text-2xs h-9 overflow-hidden"
      >
        {{ desc }}
      </p>
      <p
        class="text-gray-400 md:text-xs text-2xs group-hover:text-red-100"
        :class="subtitleClass"
      >
        {{ subtitle }}
      </p>
    </div>
  </div>
</template>
<script setup lang="ts">
import { withDefaults, reactive } from "vue";

const props = withDefaults(
  defineProps<{
    mainClass?: string;
    imgMainClass?: string;
    imgClass?: string;
    subtitleClass?: string;
    src?: string;
    title?: string;
    desc?: string;
    subtitle?: string;
  }>(),
  {
    mainClass: "flex items-center border border-gray-50 py-4",
    imgMainClass: "border-r border-gray-50 w-38",
    imgClass: "h-32",
    subtitleClass: "font-light",
  }
);
</script>
