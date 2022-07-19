<template>
  <div class="relative" :class="mainClass">
    <div>
      <div class="flex items-center justify-center" :class="imgMainClass">
        <img :src="src" alt="products" :class="imgClass" />
      </div>
    </div>
    <div
      class="absolute md:top-4 top-2.5 md:left-3 left-2 bg-black rounded text-white text-opacity-90 lg:text-xs text-2xs font-normal py-1"
      :class="tagClass"
    >
      {{ tag }}
    </div>
    <div
      class="md:px-3 px-1.5 py-2 space-y-1 absolute bottom-0 inset-x-0 flex items-end justify-between"
      :class="bottomClass"
    >
      <div class="space-y-1 px-1">
        <p class="font-semibold lg:text-base text-xs">
          {{ title }}
        </p>
        <p
          class="font-light md:text-xs text-2xs pb-1.5 leading-tight md:leading-tight"
          :class="desClass"
        >
          {{ desc }}
        </p>
      </div>
      <div v-if="icon">
        <ArrowRightIcon class="lg:w-11 w-7" />
      </div>
    </div>
  </div>
</template>
<script setup lang="ts">
import { withDefaults, reactive } from "vue";
import { ArrowRightIcon } from "@heroicons/vue/outline";

const props = withDefaults(
  defineProps<{
    mainClass?: string;
    imgMainClass?: string;
    imgClass?: string;
    subtitleClass?: string;
    src?: string;
    title?: string;
    desc?: string;
    tag?: string;
    tagClass?: string;
    icon?: boolean;
    bottomClass?: string;
    desClass?: string;
  }>(),
  {}
);
</script>
