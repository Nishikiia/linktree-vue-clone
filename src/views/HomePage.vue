<script setup>
import { ref } from 'vue'
import LinkCard from '@/components/LinkCard.vue'

const profile = ref({
  name: 'Britney Balderas',
  slogan: 'Gamer',
  avatar: 'https://api.dicebear.com/9.x/lorelei/svg',
  links: [
    {
      id: 1,
      title: 'Github',
      url: 'https://github.com/?Nishikiia',
      icon: 'code',
      description: 'Check out my projects',
    },
    {
      id: 2,
      title: 'LinkedIn',
      url: 'https://www.linkedin.com/in/britney-balderas-a474ab360/',
      icon: 'briefcase',
      description: 'Connect with me professionally',
    },
    {
      id: 3,
      title: 'Expense Splitter',
      url: 'https://expense-splitter-vue.expense-splitter-vue88532.workers.dev/',
      icon: 'calculator',
      description: 'Vue expense tracking app',
    },
  ],
})
</script>

<template>
  <main class="flex min-h-screen flex-col items-center px-4 py-8">
    <!--Profile Header-->
    <div class="mb-8 flex flex-col items-center text-center">
      <div
        class="mb-4 h-24 w-24 overflow-hidden rounded-full border-4 border-green-400 shadow-lg shadow-green-500/20"
      >
        <img
          :src="profile.avatar"
          :alt="profile.name"
          class="h-full w-full object-cover"
        />
      </div>
      <h1 class="sm.text-3xl mb-2 font-display text-2xl font-bold text-white">
        {{ profile.name }}
      </h1>
      <p class="sm:text:lg max-w-xs text-gray-300">{{ profile.slogan }}</p>
    </div>

    <!-- Link List -->
    <div class="flex w-full max-w-md flex-col gap-4">
      <LinkCard
        v-for="link in profile.links"
        :key="link.id"
      />
    </div>

    <!-- Navigate to Info-->
    <RouterLink
      to="/info"
      class="text-small mt-8 text-gray-400 underline-offset-4 transition-colors duration-200 hover:text-green-400 hover:underline"
      >About me 👉🏻</RouterLink
    >
  </main>
</template>
