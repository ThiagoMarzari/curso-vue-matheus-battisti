<template>
  <div>
    <button class="rounded-lg border px-4 py-2" @click="ativar">Clique aqui!</button>
    <span v-show="ativou">Ativado!</span>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

defineOptions({
  name: 'ReutilizacaoComponent',
})

const ativou = ref(false)

const ativar = () => {
  ativou.value = !ativou.value
}
</script>
