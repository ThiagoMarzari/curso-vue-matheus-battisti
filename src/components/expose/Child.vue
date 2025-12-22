<template>
  <div class="flex w-full items-center justify-center">
    <slot />
    <slot name="test" />
  </div>
</template>

<script setup lang="ts">
defineOptions({ name: 'ChildComponent' })

const onClick = () => {
  console.log('Opa')
}

defineExpose({ onClick })
</script>
