<template>
  <section class="relative flex items-center justify-center bg-gray-800 text-white" style="min-height: 500px;">
    <!-- Canvas para las partículas -->
    <canvas id="particles-canvas" class="absolute top-0 left-0 w-full h-full"></canvas>
    
    <div class="relative z-10 text-center max-w-2xl">
      <h1 class="text-4xl md:text-5xl font-bold mb-4">Titular Principal</h1>
      <h2 class="text-2xl md:text-3xl font-semibold mb-4">Subtítulo Atractivo</h2>
      <p class="text-lg md:text-xl mb-6">Aquí puedes describir los beneficios principales de tu servicio:</p>
      <ul class="flex space-x-4 items-center">
  <li class="flex items-center space-x-2">
    <span class="inline-block w-2 h-2 bg-white rounded-full"></span>
    <span>Bullet Point 1 con información clave.</span>
  </li>
  <li class="flex items-center space-x-2">
    <span class="inline-block w-2 h-2 bg-white rounded-full"></span>
    <span>Bullet Point 2 que destaca una característica.</span>
  </li>
  <li class="flex items-center space-x-2">
    <span class="inline-block w-2 h-2 bg-white rounded-full"></span>
    <span>Bullet Point 3 que resalta el valor.</span>
  </li>
</ul>

    </div>
  </section>
</template>

<script setup>
import { onMounted, ref } from 'vue'

onMounted(() => {
  if (process.client) {
    const canvas = document.getElementById('particles-canvas')
    const ctx = canvas.getContext('2d')
    let particlesArray = []
    const numberOfParticles = 100

    // Ajuste del tamaño del canvas
    canvas.width = window.innerWidth
    canvas.height = window.innerHeight

    window.addEventListener('resize', () => {
      canvas.width = window.innerWidth
      canvas.height = window.innerHeight
    })

    class Particle {
      constructor(x, y, directionX, directionY, size, color) {
        this.x = x
        this.y = y
        this.directionX = directionX
        this.directionY = directionY
        this.size = size
        this.color = color
      }

      draw() {
        ctx.beginPath()
        ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2, false)
        ctx.fillStyle = this.color
        ctx.fill()
      }

      update() {
        if (this.x + this.size > canvas.width || this.x - this.size < 0) {
          this.directionX = -this.directionX
        }
        if (this.y + this.size > canvas.height || this.y - this.size < 0) {
          this.directionY = -this.directionY
        }
        this.x += this.directionX
        this.y += this.directionY
        this.draw()
      }
    }

    function init() {
      particlesArray = []
      for (let i = 0; i < numberOfParticles; i++) {
        const size = Math.random() * 5 + 1
        const x = Math.random() * (canvas.width - size * 2) + size
        const y = Math.random() * (canvas.height - size * 2) + size
        const directionX = (Math.random() * 2) - 1
        const directionY = (Math.random() * 2) - 1
        const color = '#c1c1c1'

        particlesArray.push(new Particle(x, y, directionX, directionY, size, color))
      }
    }

    function animate() {
      ctx.clearRect(0, 0, canvas.width, canvas.height)

      particlesArray.forEach(particle => {
        particle.update()
      })

      requestAnimationFrame(animate)
    }

    // Añadir un efecto de sacudida al mover el mouse
    window.addEventListener('mousemove', (e) => {
      const mouseX = e.clientX
      const mouseY = e.clientY

      particlesArray.forEach(particle => {
        const dx = particle.x - mouseX
        const dy = particle.y - mouseY
        const distance = Math.sqrt(dx * dx + dy * dy)

        if (distance < 100) {
          particle.directionX = (particle.x - mouseX) / 10
          particle.directionY = (particle.y - mouseY) / 10
        }
      })
    })

    init()
    animate()
  }
})
</script>

<style scoped>
#particles-canvas {
  position: absolute;
  width: 100%;
  height: 100%;
  z-index: 1;
  display: block;
  overflow: hidden;
}
</style>
