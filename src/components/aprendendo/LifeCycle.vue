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
  <h1 class="text-4xl">Meu nome eh: {{ nome }}</h1>

  <button class="rounded-lg border p-4" @click="nome = 'Juca'">Click me</button>
</template>
