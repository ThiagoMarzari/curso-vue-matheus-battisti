<template>
  <Header :isSigned="false" />
  <Pessoa />

  <MultiplosEventos firstText="texto 1" secondText="texto 2" :delay="500" />
</template>

<script setup lang="ts">
import Header from './components/aprendendo/Header.vue'
import MultiplosEventos from './components/aprendendo/MultiplosEventos.vue'
import Pessoa from './components/aprendendo/Pessoa.vue'
</script>
