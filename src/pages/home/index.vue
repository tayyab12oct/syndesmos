<template>
  <div>
    <TopBar />
    <Hero />
    <div
      class="2xl:px-1.5 md:px-5 px-3 max-w-8xl mx-auto space-y-4 md:py-6 py-3"
    >
      <div class="">
        <h1 class="text-black md:text-xl text-lg pb-4 pt-5">Products</h1>
        <div class="grid grid-cols-5 gap-6">
          <Product />
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
</script>
