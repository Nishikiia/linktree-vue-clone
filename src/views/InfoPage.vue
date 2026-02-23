<script setup>
import { ref } from 'vue'

const bio = ref({
  name: 'Britney Balderas',
  avatar: 'https://api.dicebear.com/9.x/lorelei/svg',
  about: `I'm a gamer, hard-worker, cat mom, and gardener.`,
  skills: ['Vue.js', 'React', 'TypeScript', 'Node.js', 'Tailwind CSS'],
  email: 'camobrit@gmail.com',
  location: 'Mission, TX',
})
</script>

<template>
  <main class="flex min-h-screen flex-col items-center px-4 py-8 sm:py-12">
    <!-- Back navigation -->
    <RouterLink
      to="/"
      class="my-8 self-start text-sm text-gray-400 underline-offset-4 transition-colors duration-200 hover:text-green-400 hover:underline"
    >
      👈🏻 Back to Links
    </RouterLink>

    <!-- Profile Card -->
    <div
      class="w-full max-w-lg rounded-2xl border border-gray-700 bg-gray-800 p-6 shadow-xl shadow-gray-900/50 sm:p-8"
    >
      <!-- Steps 3–6 go inside here -->
    </div>
  </main>
</template>
