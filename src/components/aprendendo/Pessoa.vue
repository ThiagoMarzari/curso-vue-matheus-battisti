<script setup lang="ts">
import { ref } from 'vue'
import Info from './Info.vue'
import Form from './Form.vue'
import Picture from './Picture.vue'

defineOptions({
  name: 'PessoaComponent',
})

const nome = ref('Thiago')
</script>

<template>
  {{ nome }}
  <Info />
  <Form />
  <Picture />
</template>
