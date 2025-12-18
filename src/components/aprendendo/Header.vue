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
  <header class="w-full flex bg-gray-900 text-white px-4 py-8">
    <ul
      v-for="item in headerElements"
      :key="item.id"
      class="flex w-full items-center justify-center"
    >
      <li>
        <a class="hover:text-green-500 hover:cursor-pointer">{{ item.nome }}</a>
      </li>
    </ul>
  </header>
</template>
