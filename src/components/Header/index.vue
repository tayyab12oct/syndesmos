<template>
  <div
    class="border-b-3 border-gray-50 md:px-5 px-3 py-2.5 md:grid grid-cols-8 items-end flex justify-between"
  >
    <div class="col-span-2 xl:col-span-1">
      <img
        class="2xl:h-11 md:h-10 h-9"
        src="/logo/syndesmos.svg"
        alt="Syndesmos"
      />
    </div>
    <div class="xl:col-span-3 col-span-2 flex items-center space-x-2">
      <MenuAlt1Icon
        class="2xl:w-9 w-7 text-gray-200 rotate-180 cursor-pointer"
      />
      <p class="cursor-pointer font-light hidden md:inline">Menu</p>
    </div>
    <div class="col-span-4 flex items-end space-x-2">
      <div class="w-full hidden md:inline">
        <input
          type="search"
          placeholder="Search"
          class="border-b border-gray-200 focus:outline-none py-1.5 font-light text-sm w-full"
        />
      </div>
      <div class="flex items-end justify-end space-x-0.5 2xl:w-48 w-40">
        <img src="/icons/search.png" alt="search" class="2xl:w-8 w-6" />
        <img src="/icons/like.png" alt="like" class="2xl:w-9 w-7" />
        <img src="/icons/user.png" alt="user" class="2xl:w-8 w-6" />
        <img src="/icons/cart.png" alt="cart" class="2xl:w-10 w-7 -mb-1" />
      </div>
    </div>
  </div>
</template>
<script setup>
import { MenuAlt1Icon } from "@heroicons/vue/outline";
</script>
