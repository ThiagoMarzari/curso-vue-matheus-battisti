<script setup lang="ts">
defineOptions({
  name: 'HeaderComponent',
})

const headerElements = [
  { id: 1, nome: 'Home' },
  { id: 1, nome: 'Projetos' },
  { id: 1, nome: 'Contatos' },
]
</script>

<template>
  <header class="bg-gray-900 text-white px-4 py-8 w-full flex">
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
