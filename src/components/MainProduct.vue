<script setup>
defineProps({
  details: Object,
});
</script>

<template>
  <div
    class="w-1/5 bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700 m-2"
  >
    <a href="#">
      <img
        class="rounded-t-lg object-cover w-full h-60"
        :src="details.image"
        alt=""
      />
    </a>
    <div class="p-5">
      <a href="#">
        <h5
          class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white"
        >
          {{ details.name }}
        </h5>
      </a>
      <p class="mb-3 font-normal text-yellow-400">
        {{ details.stars }}
        <i
          v-for="star in new Array(parseInt(details.stars))"
          class="bi bi-star-fill"
        ></i>
        <i
          v-if="details.stars - Math.floor(details.stars) > 0"
          class="bi bi-star-half"
        ></i>
      </p>
      <p class="mb-3 font-normal text-gray-300">Sales: {{ details.sales }}</p>
      <p class="mb-3 font-normal text-gray-300">Price: {{ details.price }}$</p>
      <p class="mb-3 font-sm text-gray-700">{{ details.date }}</p>
      <a
        href="#"
        class="inline-flex items-center px-3 py-2 mx-3 text-sm font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
      >
        Cart
        <i class="bi bi-cart"></i
      ></a>
      <a
        href="#"
        class="inline-flex items-center px-3 py-2 mx-3 text-sm font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
      >
        Buy now
      </a>
    </div>
  </div>
</template>

<style>
@tailwind base;
@tailwind components;
@tailwind utilities;
</style>
