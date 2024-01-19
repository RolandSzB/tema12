<script setup>
defineEmits(["sortTopRated", "sortPopular", "sortPrice", "sortNewest"]);
defineProps({
  sortSens: String,
});
</script>

<template>
  <div class="flex justify-end items-center">
    <p class="text-xl font-bold">Sort by:</p>
    <button
      class="m-3 px-3 py-1 bg-slate-500 rounded-xl"
      @click="$emit('sortTopRated')"
    >
      Top rated
      <i v-if="sortSens === 'asc'" class="bi bi-arrow-up"></i>
      <i v-else class="bi bi-arrow-down"></i>
    </button>
    <button
      class="m-3 px-3 py-1 bg-slate-500 rounded-xl"
      @click="$emit('sortPopular')"
    >
      Popular
      <i v-if="sortSens === 'asc'" class="bi bi-arrow-up"></i>
      <i v-else class="bi bi-arrow-down"></i>
    </button>
    <button
      class="m-3 px-3 py-1 bg-slate-500 rounded-xl"
      @click="$emit('sortPrice')"
    >
      Price
      <i v-if="sortSens === 'asc'" class="bi bi-arrow-up"></i>
      <i v-else class="bi bi-arrow-down"></i>
    </button>
    <button
      class="m-3 px-3 py-1 bg-slate-500 rounded-xl"
      @click="$emit('sortNewest')"
    >
      Newest
      <i v-if="sortSens === 'asc'" class="bi bi-arrow-up"></i>
      <i v-else class="bi bi-arrow-down"></i>
    </button>
  </div>
</template>

<style></style>
