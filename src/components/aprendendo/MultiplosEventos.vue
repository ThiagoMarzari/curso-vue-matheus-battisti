<script setup lang="ts">
import { ref } from 'vue'

interface MultiplosEventosProps {
  firstText: string
  secondText: string
  delay: number
}

const { firstText, secondText, delay } = defineProps<MultiplosEventosProps>()

defineOptions({
  name: 'MultiplosEventosComponent',
})

const multiplosEventos = ref('')

const first = (txt: string, e: PointerEvent) => {
  console.log(e)
  multiplosEventos.value = txt
}

const second = (txt: string, e: PointerEvent) => {
  setTimeout(() => {
    multiplosEventos.value = txt
  }, delay)

  console.log(e)
}

const handleMultipleEvents = (event: PointerEvent) => {
  first(firstText, event)
  second(secondText, event)
}
</script>

<template>
  <div class="space-y-2">
    <button
      @click="handleMultipleEvents"
      class="rounded-lg border px-4 py-2 transition-colors hover:bg-gray-100"
    >
      Ativar multiplos eventos
    </button>
    <p>{{ multiplosEventos }}</p>
  </div>
</template>
