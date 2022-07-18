<template>
  <div class="grid grid-cols-2 md:gap-0 lg:pb-10 md:pb-5">
    <div
      v-for="v in data"
      :key="v"
      class="group relative lg:h-[520px] md:h-[400px] h-[200px] overflow-hidden"
    >
      <img
        :src="v.src"
        alt="product"
        class="w-full h-full absolute inset-0 scale-110 scale-x-125"
      />
      <div
        class="relative h-full md:p-5 px-3 md:py-7 lg:pt-14 py-4 w-full flex flex-col justify-between text-white uppercase bg-gray-40"
        :class="v.class"
      >
        <div>
          <p
            class="lg:text-[23px] md:text-base text-xs font-light tracking-wide"
          >
            {{ v.title }}
          </p>
          <h1
            class="lg:text-[170px] md:text-[125px] text-[70px] leading-none tracking-wide font-extrabold"
          >
            {{ v.no }}
          </h1>
        </div>
        <p
          class="lg:text-[22px] md:text-base text-xs tracking-wide px-4.5 pb-2"
        >
          #{{ v.tag }}
        </p>
      </div>
    </div>
  </div>
</template>
<script setup lang="ts">
import { withDefaults, reactive } from "vue";
const props = withDefaults(
  defineProps<{
    className?: string;
  }>(),
  {
    className: "",
  }
);
const data = reactive([
  {
    src: "arrivals/img1.png",
    class: "items-end text-right",
    title: "new arrivals",
    no: "20",
    tag: "Covid-19 Prevention",
  },
  {
    src: "arrivals/img2.png",
    class: "items-start",
    title: "exclusive",
    no: "22",
    tag: "Covid-19 Prevention",
  },
]);
</script>
