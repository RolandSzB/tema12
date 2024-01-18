<script setup>
defineEmits(["sortTopRated", "sortPopular", "sortPrice", "sortNewest"]);
</script>

<template>
  Sort by:
  <div>
    <button @click="$emit('sortTopRated')">Top rated</button>
    <button @click="$emit('sortPopular')">Popular</button>
    <button @click="$emit('sortPrice')">Price</button>
    <button @click="$emit('sortNewest')">Newest</button>
  </div>
</template>

<style></style>
