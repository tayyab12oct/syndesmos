<template>
  <div>
    <TopBar />
    <div class="md:px-4 px-3 max-w-8xl mx-auto space-y-4 md:py-6 py-3">
      <Arrivals />
      <Services />
      <Feed />
      <Newsletter />
    </div>
    <!-- <Footer /> -->
  </div>
</template>
<script setup>
import TopBar from "../../components/TopBar/index.vue";
import Arrivals from "../../components/Arrivals/index.vue";
import Services from "../../components/Services/index.vue";
import Feed from "../../components/Feed/index.vue";
import Newsletter from "../../components/Newsletter/index.vue";
import Footer from "../../components/Footer/index.vue";
</script>
