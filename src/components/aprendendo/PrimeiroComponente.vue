<template>
  <p>Meu nome eh: {{ nome }} e profissao: {{ profissao }}</p>
  <Reutilizacao />
  <Reutilizacao />
</template>

<script setup lang="ts">
import { ref } from 'vue'
import Reutilizacao from './Reutilizacao.vue'

defineOptions({
  name: 'PrimeiroComponente',
})

const nome = ref('Thiago')
const profissao = ref('Programador')
</script>
