<template>
  <header class="flex w-full bg-gray-900 px-4 py-6 text-white">
    <nav class="mx-auto w-full max-w-7xl">
      <ul class="flex items-center justify-between">
        <div>
          <!-- Deixar sem a div ou com div ? -->
          <img
            src="/user.jpeg"
            alt="Logo site"
            class="animate h-10 w-10 rounded-full transition-all hover:scale-105 hover:animate-bounce"
          />
        </div>
        <div class="flex gap-8">
          <li v-for="link in navLinks" :key="link.id">
            <a :href="link.href" class="transition-colors hover:text-green-500">
              {{ link.name }}
            </a>
          </li>
        </div>
        <li>
          <a v-if="isSigned" href="/perfil" class="transition-colors hover:text-green-500">
            Meu perfil
          </a>
          <a
            v-else
            href="/login"
            class="rounded-lg bg-green-500 px-4 py-2 transition-colors hover:bg-green-600"
          >
            Fazer Login
          </a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script setup lang="ts">
interface HeaderProps {
  isSigned: boolean
}

defineOptions({ name: 'HeaderComponent' })
defineProps<HeaderProps>()

const navLinks = [
  { id: 1, name: 'Home', href: '#' },
  { id: 2, name: 'Projetos', href: '#' },
  { id: 3, name: 'Contatos', href: '#' },
]
</script>
