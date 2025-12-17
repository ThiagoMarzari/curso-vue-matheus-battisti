<script setup lang="ts">
import { onBeforeMount, onMounted, onUnmounted, onUpdated, ref } from 'vue'

defineOptions({ name: 'LifeCycle' })

const nome = ref('No name ')

onBeforeMount(() => {
  console.log('Antes de montar')
})

onMounted(() => {
  nome.value = 'Thiago Marza'
})

onUpdated(() => {
  console.log('O nome foi alterado')
})

onUnmounted(() => {
  console.log('Componente desmontado')
})
</script>

<template>
  <h1>Meu nome eh: {{ nome }}</h1>

  <button class="border p-4 rounded-lg" @click="nome = 'Juca'">Click me</button>
</template>
