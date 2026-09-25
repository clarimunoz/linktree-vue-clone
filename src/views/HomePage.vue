,
<script setup>
  import { ref } from 'vue'
  import LinkCard from '@/components/LinkCard.vue'

  const profile = ref({
    name: 'Claritza Munoz',
    slogan: 'Full Stack Developer and Student',
    avatar:
      'https://api.dicebear.com/10.x/adventurer/svg?detailsVariant=&earringsVariant=&eyebrowsVariant=variant10&eyesVariant=variant13&glassesVariant=variant02&glassesProbability=100&hairColor=dba3be&skinColor=ecad80&mouthVariant=variant01&hairVariant=long08&seed=20xcw94q',
    links: [
      {
        id: 1,
        title: 'GitHub',
        url: 'https://github.com/clarimunoz',
        icon: 'code',
        description: 'Check out my projects',
      },
      {
        id: 2,
        title: 'LinkedIn',
        url: 'https://www.linkedin.com/in/claritza-munoz',
        icon: 'briefcase',
        description: 'Connect with me professionally',
      },
      {
        id: 3,
        title: 'Chip In Project',
        url: 'https://267a6151.expenses-html-bnj.pages.dev/',
        icon: 'money',
        description: 'Front-end Project to split expenses',
      },
    ],
  })
</script>

<template>
  <main class="flex min-h-screen flex-col items-center px-4 py-8">
    <!--Profile Header-->
    <div class="mb-8 flex flex-col items-center text-center">
      <div
        class="h-24 w-24 overflow-hidden rounded-full border-4 border-pink-400 shadow-lg shadow-pink-500/20 sm:w-32"
      >
        <img
          :src="profile.avatar"
          :alt="profile.name"
          class="h-full w-full object-cover"
        />
      </div>
      <h1 class="mb-2 font-display text-2xl font-bold text-white sm:text-3xl">
        {{ profile.name }}
      </h1>
      <p class="max-w-xs text-gray-300 sm:text-lg">{{ profile.slogan }}</p>
    </div>

    <!-- Link List -->
    <div class="flex w-full max-w-md flex-col gap-4">
      <LinkCard
        v-for="link in profile.links"
        :key="link.id"
        :title="link.title"
        :url="link.url"
        :description="link.description"
        :icon="link.icon"
      />
    </div>

    <!-- Navigate to Info -->
    <RouterLink
      to="/info"
      class="mt-8 text-sm text-gray-400 underline-offset-4 transition-colors duration-200 hover:text-pink-400 hover:underline"
    >
      About Me →
    </RouterLink>
  </main>
</template>
