<template>
  <div class="grid grid-cols-1 sm:grid-cols-3 gap-6 p-4">
    <List
      v-for="(card, index) in cards"
      :key="index"
      :title="card.title"
      :text="card.text"
      :image="card.image"
    />
  </div>
</template>

<script setup>
import List from "./List.vue";

const cards = [
  {
    title: "Innovation",
    text: "Pushing the limits of tech.",
    image: new URL("../assets/scroll-1.avif", import.meta.url).href,
  },
  {
    title: "Creativity",
    text: "Where ideas become reality.",
    image: new URL("../assets/scroll-2.avif", import.meta.url).href,
  },
  {
    title: "Sustainability",
    text: "Building a better future.",
    image: new URL("../assets/scroll-3.avif", import.meta.url).href,
  },
];
</script>

<style lang="scss" scoped></style>
