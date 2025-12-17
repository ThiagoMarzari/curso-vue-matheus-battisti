<script setup lang="ts">
import { ref } from 'vue'

defineOptions({
  name: 'PrimeiroComponente',
})

const nome = ref('Thiago')
const profissao = ref('Programador')
</script>

<template>
  <h1>Hello World</h1>
  <p>Meu nome eh: {{ nome }} e profissao: {{ profissao }}</p>
</template>
