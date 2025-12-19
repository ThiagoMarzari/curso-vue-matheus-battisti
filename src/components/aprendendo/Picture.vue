<template>
  <img :src="avatar" :alt="description" />
</template>

<script lang="ts" setup>
import { ref } from 'vue'

defineOptions({
  name: 'PictureComponent',
})

const avatar = ref('/user.jpeg')
const description = ref('Thiago Marzari Rossato')
</script>
