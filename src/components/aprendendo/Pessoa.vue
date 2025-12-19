<template>
  <Info :email="email" :isWorking="true" name="Thiago Marzari" />
  <Form />
  <Picture />
</template>

<script setup lang="ts">
import Info from './Info.vue'
import Form from './Form.vue'
import Picture from './Picture.vue'
import { ref } from 'vue'

defineOptions({
  name: 'PessoaComponent',
})

const email = ref('thiago@teste.com')
</script>
