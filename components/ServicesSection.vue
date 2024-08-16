<template>
  <section class="min-h-[400px] py-8 bg-gray-100 text-gray-800 p-4">
    <div class="text-center mb-8">
      <h2 class="text-4xl font-bold mb-4">Nuestros Servicios</h2>
      <h3 class="text-2xl font-semibold">Lo que ofrecemos</h3>
    </div>

    <div class="flex flex-col md:flex-row justify-center items-center space-y-4 md:space-y-0 md:space-x-4">
      <Card 
        imgSrc="https://via.placeholder.com/300" 
        title="Servicio 1" 
        content="Descripción del servicio 1. Lorem ipsum dolor sit amet, consectetur adipiscing elit." 
      />
      <Card 
        imgSrc="https://via.placeholder.com/300" 
        title="Servicio 2" 
        content="Descripción del servicio 2. Lorem ipsum dolor sit amet, consectetur adipiscing elit." 
      />
      <Card 
        imgSrc="https://via.placeholder.com/300" 
        title="Servicio 3" 
        content="Descripción del servicio 3. Lorem ipsum dolor sit amet, consectetur adipiscing elit." 
      />
    </div>
  </section>
</template>

<script setup>
import Card from './Card.vue'
</script>

<style scoped>
/* Estilos adicionales si es necesario */
</style>
