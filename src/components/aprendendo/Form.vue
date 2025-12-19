<template>
  <form @submit="enviarFormulario">
    <div class="my-2 flex gap-4">
      <input
        v-model="name"
        type="text"
        placeholder="Nome"
        class="rounded-lg border border-gray-300 px-4 py-2 focus:border-blue-500 focus:outline-none"
      />
      <input
        v-model="email"
        type="email"
        placeholder="Email"
        class="rounded-lg border border-gray-300 px-4 py-2 focus:border-blue-500 focus:outline-none"
      />
      <button
        type="submit"
        class="rounded-lg bg-blue-500 px-6 py-2 text-white transition-colors hover:bg-blue-600"
      >
        Enviar
      </button>
    </div>
  </form>
</template>

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
