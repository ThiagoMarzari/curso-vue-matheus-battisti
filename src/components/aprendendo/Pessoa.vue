<template>
  <Info :email="email" isWorking name="Thiago Marzari" />
  <Form />
  <Picture />
</template>

<script setup lang="ts">
import { ref } from 'vue'
import Info from './Info.vue'
import Form from './Form.vue'
import Picture from './Picture.vue'

defineOptions({
  name: 'PessoaComponent',
})

const email = ref('thiago@teste.com')
</script>
