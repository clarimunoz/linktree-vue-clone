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
      <div class="h-24 w-24 overflow-hidden rounded-full border-4 border-green-400 shadow-lg shadow-green-500/20">
        <img :src="profile.avatar" :alt="profile.name" class="h-full w-full object-cover">
      </div>
      <h1 class="font-display">{{ profile.name }}</h1>
      <p>{{ profile.slogan }}</p>
    </div>
  </main>
</template>
