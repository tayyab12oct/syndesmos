<template>
  <div
    class="bg-gray-100 grid md:grid-cols-2 md:gap-5 gap-4 items-center lg:py-6 py-4 lg:px-9 md:px-6 px-4"
  >
    <div class="">
      <p class="lg:text-base text-sm lg:leading-5 text-gray-700">
        Sign up for our newsletter
      </p>
      <p class="lg:text-base text-sm lg:leading-5 text-gray-700 lg:pb-1">
        Anim aute id magna aliqua ad ad non deserunt sunt. Qui irure qui Lorem
      </p>
      <p class="lg:text-sm text-xs font-light leading-6 text-gray-700">
        Qui irure qui Lorem cupidatat<span class="text-red-700">*</span>
      </p>
    </div>
    <div class="">
      <form class="flex justify-end space-x-2">
        <input
          id="email-address"
          name="email-address"
          type="email"
          autocomplete="email"
          required=""
          class="w-full lg:px-6 px-4 lg:py-3 py-2.5 border border-gray-200 placeholder-gray-200 font-light max-w-sm text-xs tracking-tight bg-transparent focus:outline-none rounded-none"
          placeholder="Enter your email"
        />
        <div class="">
          <button
            type="submit"
            class="w-full bg-gray-200 flex items-center justify-center border border-gray-200 lg:px-8 px-6 lg:py-3.5 py-2.5 text-sm text-white focus:outline-none"
          >
            Submit
          </button>
        </div>
      </form>
    </div>
  </div>
</template>
