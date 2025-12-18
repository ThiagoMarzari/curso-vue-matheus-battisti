<script setup lang="ts">
import Header from './components/aprendendo/Header.vue'
import Pessoa from './components/aprendendo/Pessoa.vue'
import PrimeiroComponente from './components/aprendendo/PrimeiroComponente.vue'
</script>

<template>
  <Header :estaLogado="true" />
  <Pessoa />
  <PrimeiroComponente />
  <button type="button">asdasdsad</button>
</template>
