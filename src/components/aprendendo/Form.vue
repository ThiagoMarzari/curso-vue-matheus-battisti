<script setup lang="ts">
import { ref } from 'vue'

defineOptions({
  name: 'FormComponent',
})

const name = ref('')
const email = ref('')

const enviarFormulario = (event: SubmitEvent) => {
  event.preventDefault()

  console.log(name.value)
  console.log(email.value)
}
</script>

<template>
  <form @submit="enviarFormulario">
    <div class="my-4 flex gap-4">
      <input class="rounded-lg border px-2" type="text" v-model="name" />
      <input class="rounded-lg border px-2" type="text" v-model="email" />
      <input type="submit" class="rounded-lg border px-4 py-2" />
    </div>
  </form>
</template>
