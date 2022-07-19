<template>
  <div>
    <TopBar />
    <Header />
    <Hero />
    <div
      class="2xl:px-1.5 md:px-5 px-3 max-w-8xl mx-auto space-y-4 md:py-6 py-3 mb-5"
    >
      <h1 class="text-black md:text-xl text-lg pb-4 pt-5">New Products</h1>
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
    <Carousel
      :settings="settings"
      :breakpoints="breakpoints"
      :autoplay="4000"
      :wrap-around="true"
    >
      <Slide v-for="slide in 5" :key="slide" class="lg:px-3 px-2">
        <div
          class="carousel__item relative overflow-hidden w-full md:h-93 h-72"
        >
          <img
            src="/hero/woman-beach.png"
            alt="Apivita"
            class="h-full w-full"
          />
          <div
            class="absolute inset-0 flex flex-col justify-between items-start w-full text-white bg-gray-20 md:px-10 px-5 py-8 text-left"
          >
            <div>
              <p class="text-lg 2xl:text-xl font-light">Sales</p>
              <h1
                class="md:text-2xl text-xl 2xl:text-[28px] font-medium max-w-xs ml-auto pt-2"
              >
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
              </h1>
            </div>
            <button
              class="border px-3 py-2.5 font-light text-sm border-white text-white"
            >
              Lorem / Ipsum
            </button>
          </div>
        </div>
      </Slide>
      <template #addons>
        <Pagination />
      </template>
    </Carousel>
    <div
      class="2xl:px-1.5 md:px-5 px-3 max-w-8xl mx-auto space-y-4 md:py-6 py-3"
    >
      <div class="">
        <h1 class="text-black md:text-xl text-lg pb-6 pt-10">Category</h1>
        <CategorySlider />
      </div>
      <div class="lg:py-10 py-2">
        <h1
          class="text-primary text-center font-semibold md:text-xl text-lg md:pb-12 pb-6"
        >
          Lorem ipsum
        </h1>
        <div
          class="bg-primary grid grid-cols-3 items-center lg:px-16 md:px-10 px-5 md:py-10 py-5"
        >
          <div class="col-span-2 flex flex-col items-start lg:px-5">
            <p class="md:text-xl text-base font-light text-white tracking-wide">
              Lorem ipsum;
            </p>
            <p
              class="md:text-3xl text-base font-normal text-white md:pb-12 pb-6"
            >
              Sed urna nulla vitae augue.
            </p>
            <button
              class="border md:px-8 px-4 py-2 font-light text-sm border-white text-white"
            >
              Lorem / Ipsum
            </button>
          </div>
          <div class="flex justify-end">
            <img class="md:h-40 h-28" src="/partner.png" alt="" />
          </div>
        </div>
      </div>
      <div class="space-y-4 pb-8">
        <h1 class="text-black md:text-xl text-lg md:pb-4 pt-5">New Products</h1>
        <div class="grid md:grid-cols-4 grid-cols-2 lg:gap-6 gap-3">
          <NewProduct
            v-for="v in newProducts"
            :key="v"
            v-bind="v"
            imgClass="h-full w-full"
          />
        </div>
      </div>
      <div class="relative overflow-hidden w-full md:h-96 h-64">
        <img src="/hero/woman-beach.png" alt="Apivita" class="h-full w-full" />
        <div
          class="absolute inset-0 flex flex-col justify-between items-end w-full text-white bg-gray-20 md:px-13 px-5 md:py-12 py-6 text-right"
        >
          <div>
            <p class="text-lg 2xl:text-xl font-light">Sales</p>
            <h1
              class="md:text-2xl text-lg 2xl:text-[28px] font-medium max-w-xs ml-auto pt-2"
            >
              Lorem ipsum dolor sit amet consectetur adipisicing elit.
            </h1>
          </div>
          <button
            class="border md:px-8 px-6 md:py-2.5 py-2 font-light text-sm border-white text-white"
          >
            Lorem / Ipsum
          </button>
        </div>
      </div>
      <Brands />
      <div class="lg:py-22 py-8">
        <Quote />
      </div>
      <div class="lg:pb-12 md:pb-4 pb-4">
        <div class="flex items-center justify-between py-7">
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
      <div class="lg:pb-14 md:pb-8 pb-4">
        <p class="text-black md:text-xl text-lg pt-5">News</p>
        <p class="text-black md:text-xl text-lg pb-6">New Products</p>
        <div class="grid md:grid-cols-4 grid-cols-2 lg:gap-6 gap-3">
          <NewProduct
            v-for="v in newProducts2"
            :key="v"
            v-bind="v"
            imgClass="h-full w-full"
            :icon="true"
          />
        </div>
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
import Header from "../../components/Header/index.vue";
import Hero from "../../components/Hero/index.vue";
import Product from "../../components/common/product/index.vue";
import NewProduct from "../../components/common/new-product/index.vue";
import CategorySlider from "../../components/category-slider/index.vue";
import Brands from "../../components/Brands/index.vue";
import Quote from "../../components/common/quote/index.vue";
import Arrivals from "../../components/Arrivals/index.vue";
import Services from "../../components/Services/index.vue";
import Feed from "../../components/Feed/index.vue";
import Newsletter from "../../components/Newsletter/index.vue";
import Footer from "../../components/Footer/index.vue";
import { Carousel, Pagination, Slide } from "vue3-carousel";

import { reactive } from "vue";
const settings = reactive({
  snapAlign: "center",
});
const breakpoints = reactive({
  200: {
    itemsToShow: 1,
  },
  500: {
    itemsToShow: 1,
  },
  700: {
    itemsToShow: 1.3,
  },
  1024: {
    itemsToShow: 1.5,
  },
  1280: {
    itemsToShow: 1.7,
  },
});
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
const newProducts = reactive([
  {
    src: "/brands/img6.png",
    title: "20 March, 2021",
    desc: "Muscleback Swimmsuit Blue/Black",
    mainClass: "col-span-2 row-span-2 text-white",
    tag: "New Products",
    tagClass: "px-4",
  },
  {
    src: "/brands/img6.png",
    title: "20 March, 2021",
    desc: "Muscleback Swimmsuit Blue/Black",
    mainClass: "text-white",
    tag: "2%",
    tagClass: "px-3",
  },
  {
    src: "/brands/img6.png",
    title: "20 March, 2021",
    desc: "Muscleback Swimmsuit Blue/Black",
    mainClass: "text-white",
    tag: "2%",
    tagClass: "px-3",
  },
  {
    src: "/brands/img6.png",
    title: "20 March, 2021",
    desc: "Muscleback Swimmsuit Blue/Black",
    mainClass: "text-white",
    tag: "2%",
    tagClass: "px-3",
  },
  {
    src: "/brands/img6.png",
    title: "20 March, 2021",
    desc: "Muscleback Swimmsuit Blue/Black",
    mainClass: "text-white",
    // bottomClass: "bg-primary pt-4",
    tag: "2%",
    tagClass: "px-3",
  },
]);
const newProducts2 = reactive([
  {
    src: "/brands/img6.png",
    title: "20 March, 2021",
    desc: "Muscleback Swimmsuit Blue/Black",
    mainClass: "col-span-2 row-span-2 text-white",
    tag: "New Products",
    tagClass: "px-4",
  },
  {
    src: "/brands/img6.png",
    title: "20 March, 2021",
    desc: "Muscleback Swimmsuit Blue Swimmsuit Muscleback Blue/Black Muscleback Swimmsuit Blue/Black",
    mainClass: "text-gray-200 border-3 border-gray-50",
    bottomClass: "lg:pt-4 pt-3 lg:pl-3 pl-2",
    desClass: "md:h-12 h-10 overflow-hidden",
    tag: "News",
    tagClass: "px-2.5",
  },
  {
    src: "/brands/img6.png",
    title: "20 March, 2021",
    desc: "Muscleback Swimmsuit Blue/Black",
    mainClass: "text-white",
    bottomClass: "bg-primary lg:pt-4 pt-3 lg:pl-4 pl-2",
    desClass: "md:h-12 h-10 overflow-hidden",
    tag: "News",
    tagClass: "px-2.5",
  },
  {
    src: "/brands/img6.png",
    title: "20 March, 2021",
    desc: "Muscleback Swimmsuit Blue/Black Swimmsuit",
    mainClass: "text-gray-200 border-3 border-gray-50",
    bottomClass: "lg:pt-4 pt-3 lg:pl-4 pl-2",
    tag: "News",
    tagClass: "px-2.5",
  },
  {
    src: "/brands/img6.png",
    title: "20 March, 2021",
    desc: "Muscleback Swimmsuit Blue/Black Swimmsuit",
    mainClass: "text-white",
    bottomClass: "bg-primary lg:pt-4 pt-3 lg:pl-4 pl-2",
    tag: "News",
    tagClass: "px-2.5",
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
<style>
.carousel__pagination {
  @apply pt-3;
}
.carousel__pagination .carousel__pagination-item .carousel__pagination-button {
  @apply h-2.5 w-2.5 rounded-full;
}
.carousel__pagination-button {
  @apply bg-gray-20;
}
.carousel__pagination-button--active {
  @apply bg-red-600;
}
</style>
