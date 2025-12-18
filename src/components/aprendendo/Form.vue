<script setup lang="ts">
import { ref } from 'vue'

defineOptions({
  name: 'FormComponent',
})

const name = ref('')
const email = ref('')

function enviarFormulario(e: SubmitEvent) {
  e.preventDefault()

  console.log(name.value)
  console.log(email.value)
}
</script>

<template>
  <form action="" @submit="enviarFormulario">
    <div class="flex gap-4 my-4">
      <input class="border px-2 rounded-lg" type="text" v-model="name" />
      <input class="border px-2 rounded-lg" type="text" v-model="email" />
      <input type="submit" class="border rounded-lg px-4 py-2" />
    </div>
  </form>
</template>
