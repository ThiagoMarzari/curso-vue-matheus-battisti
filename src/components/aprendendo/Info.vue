<template>
  <div class="border">
    <p>Nome: {{ name }}</p>
    <p>Email: {{ email }}</p>
    <p>Está trabalhando: {{ isWorking }}</p>
  </div>

  <p>Estou trabalhando no momento</p>
  <p>Utilizo as seguintes tecnologias</p>

  <ul class="my-4 border py-4">
    <li v-for="(techBack, index) in backendTechnologies" :key="index">{{ techBack }}</li>
  </ul>

  <ul class="my-4 border py-4">
    <li v-for="(techFront, index) in frontendTechnologies" :key="index">{{ techFront }}</li>
  </ul>

  <p v-if="isWorking">Thiago atualmente está trabalhando</p>
  <p v-else>Nao está trabalhando {{ isWorking }}</p>
  <p v-if="1 > 2">Teste</p>

  <button
    @click="toggleEmail"
    class="my-4 rounded-lg border px-4 py-2 transition-all hover:border-red-500"
  >
    Mostrar email
  </button>

  <p v-show="showEmail">Email: {{ email }}</p>

  <div v-for="(n, index) in numbers" :key="index">
    <p v-if="n <= 3">{{ n }}</p>
    <p v-else class="text-green-500">{{ n }}</p>
  </div>

  <p>Acessar meu portfolio: <a :href="link" target="_blank"> Clique aqui...</a></p>
</template>

<script setup lang="ts">
import { ref } from 'vue'

interface InfoProps {
  name: string
  email: string
  isWorking: boolean
}

defineProps<InfoProps>()

defineOptions({
  name: 'InfoComponent',
})

const numbers = [1, 2, 3, 4, 5]
const link = ref('https://jsonplaceholder.typicode.com/todos')
const backendTechnologies = ['Javasript', 'PHP', 'Python']
const frontendTechnologies = ['html', 'css', 'react']

const showEmail = ref(false)

const toggleEmail = () => {
  console.log('Mostrando email')
  showEmail.value = !showEmail.value
}
</script>
