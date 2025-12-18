<script setup lang="ts">
interface HeaderProps {
  estaLogado: boolean
}

defineOptions({ name: 'HeaderComponent' })
defineProps<HeaderProps>()

const headerElements = [
  { id: 1, nome: 'Home' },
  { id: 1, nome: 'Projetos' },
  { id: 1, nome: 'Contatos' },
]
</script>

<template>
  <header class="flex w-full bg-gray-900 px-4 py-8 text-white">
    <ul class="flex w-full items-center justify-center">
      <li v-for="item in headerElements" :key="item.id">
        <a class="hover:cursor-pointer hover:text-green-500">{{ item.nome }}</a>
      </li>
    </ul>
  </header>
</template>
