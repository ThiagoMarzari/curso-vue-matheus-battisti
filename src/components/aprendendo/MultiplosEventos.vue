<script setup lang="ts">
import { ref } from 'vue'

defineOptions({
  name: 'MultiplosEventosCompoennt',
})

const multiplosEventos = ref('')

function primeiro(txt: string, e: PointerEvent) {
  console.log(e)
  multiplosEventos.value = txt
}

function segundo(txt: string, e: PointerEvent) {
  setTimeout(() => {
    multiplosEventos.value = txt
  }, 500)

  console.log(e)
}
</script>

<template>
  <div>
    <button
      @click="(primeiro('teste 1', $event), segundo('teste 2', $event))"
      class="border rounded-lg px-4 py-2"
    >
      Ativar multiplos eventos
    </button>
    <p>{{ multiplosEventos }}</p>
  </div>
</template>
