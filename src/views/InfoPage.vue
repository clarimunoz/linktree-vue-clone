<script setup>
import { ref } from 'vue'

const bio = ref({
  name: 'Claritza Munoz',
  avatar: 'https://api.dicebear.com/10.x/adventurer/svg?detailsVariant=&earringsVariant=&eyebrowsVariant=variant10&eyesVariant=variant13&glassesVariant=variant02&glassesProbability=100&hairColor=dba3be&skinColor=ecad80&mouthVariant=variant01&hairVariant=long08&seed=20xcw94q',
  about: `I'm a passionate full-stack developer with experience building modern web applications. I specialize in Vue.js, React, Node.js, and I love creating beautiful, user-friendly interfaces that make a difference. I'm also a student at STC.`,
  skills: ['Vue.js', 'React', 'Typescript', '.NET', 'C#', 'C++', 'CSS'],
  email: 'cmunoz7@stu.southtexascollege.edu',
  location: 'McAllen, Tx'
})
</script>

<template>
  <main class="flex min-h flex-col items-center px-4 py-8 sm:py-12">
    <RouterLink to="/"
      class="my-8 self-start text-sm text-gray-400 underline-offset-4 hover:underline hover:text-green-400 hover:underline transition-colors duration-200">
      ← Back to Links
    </RouterLink>

    <!-- Profile Card -->
    <div class="w-full max-w-lg rounded-2xl border border-gray-700 bg-gray-800 p-6 shadow-xl shadow-gray-900/50 sm:p-8">

      <!-- Header -->
      <div class="mb-6 flex flex-col items-center text-center sm:flex-row sm:text-left">
        <div class="mb-4 h-20 w-20 shrink-0 overflow-hidden rounded-full border-4 border-green-400 sm:mb-0 sm:mr-6">
          <img :src="bio.avatar" :alt="bio.name" class="h-full w-full object-cover" />
        </div>
        <div>
          <h1 class="font-display mb-1 text-2xl font-bold text-white">{{ bio.name }}</h1>
          <p class="text-sm text-gray-400">📍 {{ bio.location }}</p>
        </div>
      </div>
    </div>
  </main>
</template>
