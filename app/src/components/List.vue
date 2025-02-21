<!-- src/components/Card.vue -->
<template>
    <div class="max-w-sm bg-white rounded-lg shadow-lg overflow-hidden">
      <img :src="image" :alt="title" class="w-full h-48 object-cover">
      <div class="p-4">
        <h3 class="text-lg font-semibold text-gray-900">{{ title }}</h3>
        <p class="mt-2 text-gray-600">{{ text }}</p>
      </div>
    </div>
  </template>
  
  <script setup>
  defineProps({
    title: String,
    text: String,
    image: String
  });
  </script>

<style lang="scss" scoped>
.card {
  transition: box-shadow 0.3s ease-in-out;
  box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.1);
}

.card:hover {
  box-shadow: 4px 4px 20px rgba(0, 0, 0, 0.2);
}
</style>


  

  