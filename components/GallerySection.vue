<template>
    <section class="py-8 bg-white">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <h2 class="text-4xl font-bold text-center mb-8">Galería de Imágenes</h2>
        
        <div class="gallery-grid">
          <img src="https://via.placeholder.com/400x600" alt="Gallery Image 1" class="gallery-item" />
          <img src="https://via.placeholder.com/400x300" alt="Gallery Image 2" class="gallery-item" />
          <img src="https://via.placeholder.com/400x500" alt="Gallery Image 3" class="gallery-item" />
          <img src="https://via.placeholder.com/400x700" alt="Gallery Image 4" class="gallery-item" />
          <img src="https://via.placeholder.com/400x600" alt="Gallery Image 5" class="gallery-item" />
         
          
        </div>
      </div>
    </section>
  </template>
  
  <script setup>
    // No hay lógica necesaria para este componente.
  </script>
  
  <style scoped>
  .gallery-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    gap: 16px;
  }
  
  .gallery-item {
    width: 100%;
    height: auto;
    border-radius: 8px;
    transition: transform 0.3s ease-in-out;
  }
  
  .gallery-item:hover {
    transform: scale(1.05);
  }
  </style>
  