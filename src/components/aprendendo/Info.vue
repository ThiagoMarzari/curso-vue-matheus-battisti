<script setup lang="ts">
import { ref } from 'vue'

defineOptions({
  name: 'InfoComponent',
})

const estaTrabalhando = ref(true)
const email = 'thiago@teste.com'
const mostrarEmail = ref(false)

const numeros = [1, 2, 3, 4, 5]
const meu_link = 'https://jsonplaceholder.typicode.com/todos'
const backendTechnologies = ['Javasript', 'PHP', 'Python']
const frontendTechnologies = ['html', 'css', 'react']

function toggleEmail() {
  console.log('Mostrando email')
  mostrarEmail.value = !mostrarEmail.value
}
</script>

<template>
  <p>Estou trabalhando no momento</p>
  <p>Utilizo as seguintes tecnologias</p>

  <ul class="border py-4 my-4">
    <li v-for="(tech, index) in backendTechnologies" :key="index">{{ tech }}</li>
  </ul>

  <ul class="border py-4 my-4">
    <li v-for="(tech, index) in frontendTechnologies" :key="index">{{ tech }}</li>
  </ul>

  <p v-if="estaTrabalhando">Thiago atualmente está trabalhando</p>
  <p v-else>Nao está trabalhando {{ estaTrabalhando }}</p>
  <p v-if="1 > 2">Teste</p>
  <button
    @click="toggleEmail"
    class="border rounded-lg px-4 py-2 my-4 hover:border-red-500 transition-all"
  >
    Mostrar email
  </button>
  <p v-show="mostrarEmail">Email: {{ email }}</p>

  <div v-for="(n, index) in numeros" :key="index">
    <p v-if="n <= 3">{{ n }}</p>
    <p v-else class="text-green-500">{{ n }}</p>
  </div>

  <p>Acessar meu portfolio: <a :href="meu_link" target="_blank"> Clique aqui...</a></p>
</template>
