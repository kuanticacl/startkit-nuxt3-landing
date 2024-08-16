<template>
  <section class="flex flex-col md:flex-row items-center justify-center p-8 bg-gradient-to-r from-blue-500 via-purple-600 to-pink-500 text-white">
    <!-- Lado Izquierdo: Imagen -->
    <div class="w-full md:w-1/2 h-64 md:h-80 overflow-hidden">
      <img src="https://via.placeholder.com/800x600" alt="About Image" class="w-full h-full object-cover" />
    </div>
    
    <!-- Lado Derecho: Contenido de Texto -->
    <div class="w-full md:w-1/2 flex items-center justify-center text-center p-4">
      <div>
        <h2 class="text-3xl md:text-4xl font-bold mb-4">Nuestro Compromiso</h2>
        <h3 class="text-xl md:text-2xl font-semibold mb-4">Subtítulo Atractivo</h3>
        <p class="text-lg md:text-xl">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam sit amet placerat orci, non bibendum purus. Vivamus vehicula, magna a pharetra ultricies, libero lacus vehicula ligula, id varius enim arcu nec quam.
        </p>
      </div>
    </div>
  </section>
</template>

<script setup>
  // No hay necesidad de lógica en este componente.
</script>

<style scoped>
/* Puedes agregar estilos adicionales si lo necesitas */
</style>
