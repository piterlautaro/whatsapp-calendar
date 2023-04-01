<template>
  <div class="container mx-auto p-4">
    <h1 class="text-2xl font-bold mb-4">Calendario de eventos</h1>
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-4">
      <div v-for="(evento, index) in eventos" :key="index" class="bg-white rounded-lg shadow p-4">
        <div class="flex items-center mb-2">
          <div class="rounded-full h-4 w-4 mr-2" :style="'background-color:' + evento.etiquetas[0].color"></div>
          <p class="font-bold text-sm">{{ evento.etiquetas[0].nombre }}</p>
        </div>
        <p class="text-gray-600 text-sm mb-2">{{ evento.evento }}</p>
        <div class="flex justify-between">
          <p class="text-gray-500 text-xs">{{ evento.fecha }}</p>
          <p class="text-gray-500 text-xs">{{ evento.informacion_adicional }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import calendario from '@/services/calendary.json'

export default {
  name: 'CalendaryComponent',
  data() {
    return {
      eventos: calendario
    }
  }
}
</script>

<style>
/* Aquí puedes agregar estilos personalizados si los necesitas */
</style>
