<script setup>
defineEmits(["sortTopRated", "sortPopular", "sortPrice", "sortNewest"]);
defineProps({
  sortSens: String,
  sortActive: Number,
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
      <span v-if="sortActive === 1">
        <i v-if="sortSens === 'asc'" class="bi bi-arrow-down"></i>
        <i v-else class="bi bi-arrow-up"></i
      ></span>
    </button>
    <button
      class="m-3 px-3 py-1 bg-slate-500 rounded-xl"
      @click="$emit('sortPopular')"
    >
      Popular
      <span v-if="sortActive === 2">
        <i v-if="sortSens === 'asc'" class="bi bi-arrow-down"></i>
        <i v-else class="bi bi-arrow-up"></i
      ></span>
    </button>
    <button
      class="m-3 px-3 py-1 bg-slate-500 rounded-xl"
      @click="$emit('sortPrice')"
    >
      Price
      <span v-if="sortActive === 3">
        <i v-if="sortSens === 'asc'" class="bi bi-arrow-down"></i>
        <i v-else class="bi bi-arrow-up"></i>
      </span>
    </button>
    <button
      class="m-3 px-3 py-1 bg-slate-500 rounded-xl"
      @click="$emit('sortNewest')"
    >
      Newest
      <span v-if="sortActive === 4">
        <i v-if="sortSens === 'asc'" class="bi bi-arrow-down"></i>
        <i v-else class="bi bi-arrow-up"></i>
      </span>
    </button>
  </div>
</template>

<style></style>
