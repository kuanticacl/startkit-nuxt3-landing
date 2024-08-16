<template>
    <section class="bg-gray-100 py-12">
      <div class="max-w-4xl mx-auto text-center">
        <h2 class="text-4xl font-bold mb-4">Contáctanos</h2>
        <p class="text-lg mb-8">Estamos aquí para ayudarte. Completa el formulario a continuación y nos pondremos en contacto contigo lo antes posible.</p>
        
        <form class="bg-white p-8 rounded-lg shadow-md">
          <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-4">
            <input type="text" placeholder="Nombre" class="form-input" required />
            <input type="text" placeholder="Apellido" class="form-input" required />
          </div>
          <div class="mb-4">
            <input type="tel" placeholder="Teléfono" class="form-input" required />
          </div>
          <div class="mb-4">
            <input type="text" placeholder="Asunto" class="form-input" required />
          </div>
          <div class="mb-4">
            <textarea placeholder="Consulta" class="form-input h-32" required></textarea>
          </div>
          <button type="submit" class="w-full bg-blue-500 text-white py-2 px-4 rounded hover:bg-blue-600 transition-colors">Enviar</button>
        </form>
      </div>
    </section>
  
    <!-- Footer -->
    <footer class="bg-purple-600 text-white py-6 mt-12">
      <div class="max-w-4xl mx-auto text-center">
        <p>&copy; 2024 Tu Empresa. Todos los derechos reservados.</p>
      </div>
    </footer>
  </template>
  
  <script setup>
    // No se necesita lógica adicional en este componente.
  </script>
  
  <style scoped>
  .form-input {
    width: 100%;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 4px;
    transition: border-color 0.3s;
  }
  
  .form-input:focus {
    outline: none;
    border-color: #3182ce;
  }
  </style>
  