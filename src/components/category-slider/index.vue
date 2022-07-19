<template>
  <Carousel
    :settings="settings"
    :breakpoints="breakpoints"
    :wrap-around="true"
    class="2xl:-mx-3 -mx-1.5"
  >
    <Slide v-for="slide in 12" :key="slide" class="lg:px-3 px-2">
      <div class="carousel__item flex flex-col space-y-2.5">
        <div class="flex items-center justify-center h-42">
          <img :src="src" alt="products" class="w-full h-full" />
        </div>
        <p
          class="text-gray-200 font-light text-center md:text-sm text-xs tracking-wide uppercase"
        >
          {{ title }}
        </p>
      </div>
    </Slide>
    <template #addons>
      <Navigation />
    </template>
  </Carousel>
</template>
<script setup lang="ts">
import { withDefaults, reactive } from "vue";
import { Carousel, Navigation, Slide } from "vue3-carousel";
import "vue3-carousel/dist/carousel.css";

const props = withDefaults(
  defineProps<{
    src?: string;
    title?: string;
  }>(),
  { src: "/brands/img5.png", title: "PACK" }
);

const settings = {
  itemsToShow: 1,
  snapAlign: "center",
};
const breakpoints = {
  200: {
    itemsToShow: 2,
    snapAlign: "start",
  },
  500: {
    itemsToShow: 3,
    snapAlign: "start",
  },
  700: {
    itemsToShow: 4,
    snapAlign: "start",
  },
  1024: {
    itemsToShow: 6,
    snapAlign: "start",
  },
  1280: {
    itemsToShow: 7,
    snapAlign: "start",
  },
};
</script>
<style>
.carousel__prev {
  @apply bg-white shadow left-2 top-[45%] outline-none;
}
.carousel__next {
  @apply bg-white shadow right-2 top-[45%] outline-none;
}
.carousel__icon {
  @apply text-black;
}
</style>
