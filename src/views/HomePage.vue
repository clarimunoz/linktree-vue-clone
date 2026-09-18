,
<script setup>
import { ref } from 'vue'
import LinkCard from '@/components/LinkCard.vue';

const profile = ref({
  name: 'Claritza Munoz',
  slogan: 'Full Stack Developer and Student',
  avatar: 'https://api.dicebear.com/10.x/adventurer/svg?detailsVariant=&earringsVariant=&eyebrowsVariant=variant10&eyesVariant=variant13&glassesVariant=variant02&glassesProbability=100&hairColor=dba3be&skinColor=ecad80&mouthVariant=variant01&hairVariant=long08&seed=20xcw94q'
})
</script>

<template>
  <main class="flex min-h-screen flex-col items-center px-4 py-8">
    <!--Profile Header-->
    <div class="mb-8 flex flex-col items-center text-center">
      <div
        class="h-24 w-24 overflow-hidden rounded-full border-4 border-green-400 shadow-lg shadow-green-500/20 sm:w-32">
        <img :src="profile.avatar" :alt="profile.name" class="h-full w-full object-cover">
      </div>
      <h1 class="font-display mb-2 text-2xl font-bold text-white sm:text-3xl">{{ profile.name }}</h1>
      <p class="max-w-xs text-gray-300 sm:text-lg">{{ profile.slogan }}</p>
    </div>

    <!-- Link List -->
    <div class="flex w-full mx-w-md flex-col gap-4">
      <LinkCard v-for="x of [1, 2, 3]" :key="x" />
    </div>

    <!-- Navigate to Info -->
    <RouterLink to="/info"
      class="mt-8 text-sm text-gray-400 underline-offset-4 hover:underline hover:text-green-400 hover:underline transition-colors duration-200">
      About Me →
    </RouterLink>
  </main>
</template>
