<template>
  <div class="grid grid-cols-2 md:gap-0 lg:pb-10 md:pb-5">
    <div
      v-for="v in data"
      :key="v"
      class="group relative bg-gray-50 lg:h-[500px] md:h-[400px] h-[200px]"
    >
      <img :src="v.src" alt="product" class="w-full h-full" />
      <div
        class="absolute inset-0 md:p-5 px-3 md:py-7 py-4 cursor-pointer w-full flex flex-col justify-between text-white uppercase"
        :class="v.class"
      >
        <div>
          <p
            class="lg:text-[22px] md:text-base text-xs font-light tracking-wide"
          >
            {{ v.title }}
          </p>
          <h1
            class="lg:text-[150px] md:text-[125px] text-[70px] leading-none tracking-wide font-extrabold"
          >
            {{ v.no }}
          </h1>
        </div>
        <p class="lg:text-[22px] md:text-base text-xs tracking-wide">
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
    src: "https://images.unsplash.com/photo-1517841905240-472988babdf9?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=8&w=1024&h=1024&q=80",
    class: "items-end text-right",
    title: "new arrivals",
    no: "20",
    tag: "Covid-19 Prevention",
  },
  {
    src: "https://images.unsplash.com/photo-1517841905240-472988babdf9?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=8&w=1024&h=1024&q=80",
    class: "items-start",
    title: "exclusive",
    no: "22",
    tag: "Covid-19 Prevention",
  },
]);
</script>
