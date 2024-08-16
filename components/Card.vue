<template>
  <div class="w-full md:w-1/3 bg-white rounded-lg shadow-lg overflow-hidden transform transition-transform duration-500 hover:scale-105 animate-fadeInUp">
    <img :src="imgSrc" alt="Service Image" class="w-full h-48 object-cover" />
    <div class="p-6">
      <h3 class="text-xl font-bold mb-2">{{ title }}</h3>
      <p class="text-gray-700">{{ content }}</p>
    </div>
  </div>
</template>

<script setup>
import { defineProps } from 'vue'

const props = defineProps({
  imgSrc: {
    type: String,
    required: true
  },
  title: {
    type: String,
    required: true
  },
  content: {
    type: String,
    required: true
  }
})
</script>

<style scoped>
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.animate-fadeInUp {
  animation: fadeInUp 0.5s ease-out;
}
</style>
