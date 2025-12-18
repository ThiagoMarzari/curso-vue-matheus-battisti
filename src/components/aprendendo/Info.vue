<script setup lang="ts">
import { ref } from 'vue'

interface InfoProps {
  name: string
  email: string
  estaTrabalhando: boolean
}

defineProps<InfoProps>()

defineOptions({
  name: 'InfoComponent',
})

const showEmail = ref(false)

const numeros = [1, 2, 3, 4, 5]
const meu_link = 'https://jsonplaceholder.typicode.com/todos'
const backendTechnologies = ['Javasript', 'PHP', 'Python']
const frontendTechnologies = ['html', 'css', 'react']

const toggleEmail = () => {
  console.log('Mostrando email')
  showEmail.value = !showEmail.value
}
</script>

<template>
  <div class="h-4 w-4 border">
    <p>Nome: {{ name }}</p>
    <p>Email: {{ email }}</p>
    <p>Está trabalhando: {{ estaTrabalhando }}</p>
  </div>

  <p>Estou trabalhando no momento</p>
  <p>Utilizo as seguintes tecnologias</p>

  <ul class="my-4 border py-4">
    <li v-for="(tech, index) in backendTechnologies" :key="index">{{ tech }}</li>
  </ul>

  <ul class="my-4 border py-4">
    <li v-for="(tech, index) in frontendTechnologies" :key="index">{{ tech }}</li>
  </ul>

  <p v-if="estaTrabalhando">Thiago atualmente está trabalhando</p>
  <p v-else>Nao está trabalhando {{ estaTrabalhando }}</p>
  <p v-if="1 > 2">Teste</p>
  <button
    @click="toggleEmail"
    class="my-4 rounded-lg border px-4 py-2 transition-all hover:border-red-500"
  >
    Mostrar email
  </button>
  <p v-show="showEmail">Email: {{ email }}</p>

  <div v-for="(n, index) in numeros" :key="index">
    <p v-if="n <= 3">{{ n }}</p>
    <p v-else class="text-green-500">{{ n }}</p>
  </div>

  <p>Acessar meu portfolio: <a :href="meu_link" target="_blank"> Clique aqui...</a></p>
</template>
