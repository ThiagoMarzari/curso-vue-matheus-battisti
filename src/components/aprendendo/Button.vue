<template>
  <div class="flex w-full items-center justify-center">
    <button
      @click="$emit('handleClick')"
      class="rounded-lg border bg-blue-600 px-4 py-2 text-2xl text-white"
    >
      Clique aqui
    </button>
  </div>
</template>

<script setup lang="ts">
defineOptions({ name: 'ButtonComponent' })
defineEmits<{
  (e: 'handleClick'): void
}>()
// defineEmits(['handleClick'])
</script>
