<template>
  <div>
    <TopBar />
    <Hero />
    <div
      class="2xl:px-1.5 md:px-5 px-3 max-w-8xl mx-auto space-y-4 md:py-6 py-3"
    >
      <div class="">
        <h1 class="text-black md:text-xl text-lg pb-4 pt-5">Products</h1>
        <div
          class="grid lg:grid-cols-5 md:grid-cols-3 grid-cols-2 md:gap-6 gap-4"
        >
          <Product
            v-for="v in products"
            :key="v"
            v-bind="v"
            mainClass="group"
            imgClass="h-62"
            imgMainClass="border-b-3 border-gray-50 group-hover:bg-gray-150 p-10"
            subtitleClass="font-semibold"
          />
        </div>
      </div>
      <div class="">
        <div class="flex items-center justify-between py-6">
          <h1 class="text-black md:text-2xl text-lg tracking-tight">
            Best Sellers
          </h1>
          <p
            class="text-black font-extralight md:text-base text-sm tracking-tight"
          >
            View More
          </p>
        </div>
        <div class="grid lg:grid-cols-3 md:grid-cols-2 md:gap-6 gap-4">
          <Product v-for="v in sellers" :key="v" v-bind="v" />
        </div>
      </div>
      <Brands />
      <div class="lg:py-22 py-8">
        <Quote />
      </div>
      <Arrivals />
      <Services />
      <Feed />
      <Newsletter />
    </div>
    <Footer />
  </div>
</template>
<script setup>
import TopBar from "../../components/TopBar/index.vue";
import Hero from "../../components/Hero/index.vue";
import Product from "../../components/common/product/index.vue";
import Brands from "../../components/Brands/index.vue";
import Quote from "../../components/common/quote/index.vue";
import Arrivals from "../../components/Arrivals/index.vue";
import Services from "../../components/Services/index.vue";
import Feed from "../../components/Feed/index.vue";
import Newsletter from "../../components/Newsletter/index.vue";
import Footer from "../../components/Footer/index.vue";

import { reactive } from "vue";

const products = reactive([
  {
    src: "/products/anti_hair.png",
    title: "Woman's Placement Thinstrap",
    desc: "Muscleback Swimmsuit Blue/Black",
    subtitle: "Lorem ipsum dolor sit Lorem ipsum",
  },
  {
    src: "/products/anti_hair.png",
    title: "Woman's Placement Thinstrap",
    desc: "Muscleback Swimmsuit Blue/Black",
    subtitle: "Lorem ipsum dolor sit Lorem ipsum",
  },
  {
    src: "/products/anti_hair.png",
    title: "Woman's Placement Thinstrap",
    desc: "Muscleback Swimmsuit Blue/Black",
    subtitle: "Lorem ipsum dolor sit Lorem ipsum",
  },
  {
    src: "/products/anti_hair.png",
    title: "Woman's Placement Thinstrap",
    desc: "Muscleback Swimmsuit Blue/Black",
    subtitle: "Lorem ipsum dolor sit Lorem ipsum",
  },
  {
    src: "/products/anti_hair.png",
    title: "Woman's Placement Thinstrap",
    desc: "Muscleback Swimmsuit Blue/Black",
    subtitle: "Lorem ipsum dolor sit Lorem ipsum",
  },
  {
    src: "/products/anti_hair.png",
    title: "Woman's Placement Thinstrap",
    desc: "Muscleback Swimmsuit Blue/Black",
    subtitle: "Lorem ipsum dolor sit Lorem ipsum",
  },
  {
    src: "/products/anti_hair.png",
    title: "Woman's Placement Thinstrap",
    desc: "Muscleback Swimmsuit Blue/Black",
    subtitle: "Lorem ipsum dolor sit Lorem ipsum",
  },
  {
    src: "/products/anti_hair.png",
    title: "Woman's Placement Thinstrap",
    desc: "Muscleback Swimmsuit Blue/Black",
    subtitle: "Lorem ipsum dolor sit Lorem ipsum",
  },
  {
    src: "/products/anti_hair.png",
    title: "Woman's Placement Thinstrap",
    desc: "Muscleback Swimmsuit Blue/Black",
    subtitle: "Lorem ipsum dolor sit Lorem ipsum",
  },
  {
    src: "/products/anti_hair.png",
    title: "Woman's Placement Thinstrap",
    desc: "Muscleback Swimmsuit Blue/Black",
    subtitle: "Lorem ipsum dolor sit Lorem ipsum",
  },
]);
const sellers = reactive([
  {
    src: "/products/anti_hair.png",
    title: "Woman's Placement Thinstrap",
    desc: "Muscleback Swimmsuit Blue/Black",
    subtitle: "Lorem ipsum dolor sit Lorem ipsum",
  },
  {
    src: "/products/anti_hair.png",
    title: "Woman's Placement Thinstrap",
    desc: "Muscleback Swimmsuit Blue/Black",
    subtitle: "Lorem ipsum dolor sit Lorem ipsum",
  },
  {
    src: "/products/anti_hair.png",
    title: "Woman's Placement Thinstrap",
    desc: "Muscleback Swimmsuit Blue/Black",
    subtitle: "Lorem ipsum dolor sit Lorem ipsum",
  },
  {
    src: "/products/anti_hair.png",
    title: "Woman's Placement Thinstrap",
    desc: "Muscleback Swimmsuit Blue/Black",
    subtitle: "Lorem ipsum dolor sit Lorem ipsum",
  },
  {
    src: "/products/anti_hair.png",
    title: "Woman's Placement Thinstrap",
    desc: "Muscleback Swimmsuit Blue/Black",
    subtitle: "Lorem ipsum dolor sit Lorem ipsum",
  },
  {
    src: "/products/anti_hair.png",
    title: "Woman's Placement Thinstrap",
    desc: "Muscleback Swimmsuit Blue/Black",
    subtitle: "Lorem ipsum dolor sit Lorem ipsum",
  },
]);
</script>
