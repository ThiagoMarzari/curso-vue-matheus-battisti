<template>
  <div>
    <Button @handleClick="onClick" />
  </div>
</template>

<script setup lang="ts">
defineOptions({ name: 'EmitComponent' })
import Button from './Button.vue'

const onClick = () => {
  console.log('Opa')
}
</script>
