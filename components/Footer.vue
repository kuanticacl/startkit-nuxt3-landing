<template>
    <footer :class="[full ? 'w-full' : 'max-w-screen-xl mx-auto', 'bg-gray-800 text-white text-center py-6 animate-fadeIn']">
      <p>&copy; 2024 Landing Page. All rights reserved.</p>
    </footer>
  </template>
  
  <script setup>
  import { defineProps } from 'vue'
  
  const props = defineProps({
    full: {
      type: Boolean,
      default: false
    }
  })
  </script>
  