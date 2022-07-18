<template>
  <div>
    <h1 class="text-black md:text-xl text-lg pb-4 pt-5">Brands</h1>
    <div
      class="grid lg:grid-cols-4 md:grid-cols-3 grid-cols-2 lg:gap-6 md:gap-3 gap-2"
    >
      <div class="relative lg:h-80 md:h-60 h-40" v-for="v in brands" :key="v">
        <img :src="v.src" alt="" class="h-full w-full" v-if="v.src" />
        <div :class="v.bgColor" class="h-full w-full" v-else></div>
        <div
          class="flex items-center justify-center absolute inset-0 p-6"
          :class="v.brandImg ? 'bg-gray-40' : ''"
        >
          <img :src="v.brandImg" alt="" />
        </div>
      </div>
    </div>
    <p class="text-center text-gray-600 font-light md:text-lg text-base pt-6">
      Lorem ipsum
    </p>
  </div>
</template>
<script setup>
import { reactive } from "vue";

const brands = reactive([
  {
    src: "/brands/img1.png",
    brandImg: "/brands/kanavos.png",
  },
  {
    bgColor: "bg-indigo-900",
    brandImg: "/brands/galesyn.png",
  },
  {
    src: "/brands/img2.png",
    brandImg: "/brands/kanavos.png",
  },
  {
    bgColor: "bg-red-800",
    brandImg: "/brands/kanavos.png",
  },
  {
    src: "/brands/img5.png",
    brandImg: "/brands/hartmann.png",
  },
  {
    src: "/brands/img4.png",
    brandImg: "/brands/matsuda.png",
  },
  {
    src: "/brands/img5.png",
    brandImg: "/brands/chemco.png",
  },
  {
    src: "/brands/img6.png",
    brandImg: "/brands/apivita.png",
  },
]);
</script>
