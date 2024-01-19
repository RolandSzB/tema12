<script setup>
defineEmits(["sortTopRated", "sortPopular", "sortPrice", "sortNewest"]);
</script>

<template>
  <div class="flex justify-end items-center">
    <p class="text-xl font-bold">Sort by:</p>
    <button
      class="m-3 px-3 py-1 bg-slate-500 rounded-xl"
      @click="$emit('sortTopRated')"
    >
      Top rated
    </button>
    <button
      class="m-3 px-3 py-1 bg-slate-500 rounded-xl"
      @click="$emit('sortPopular')"
    >
      Popular
    </button>
    <button
      class="m-3 px-3 py-1 bg-slate-500 rounded-xl"
      @click="$emit('sortPrice')"
    >
      Price
    </button>
    <button
      class="m-3 px-3 py-1 bg-slate-500 rounded-xl"
      @click="$emit('sortNewest')"
    >
      Newest
    </button>
  </div>
</template>

<style></style>
