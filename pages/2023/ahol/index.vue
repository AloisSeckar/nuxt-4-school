<template>
  <div>
    <h2>VOŠ AHOL, Ostrava - 20.11.2023</h2>
    <div>
      Výsledky workshopu:
    </div>
    <ul class="list-disc pl-6">
      <li v-for="item in profiles" :key="item.link">
        <NuxtLink :to="`/demo/${item.link}`">
          <strong>{{ item.name }}</strong>
        </NuxtLink>
      </li>
      <li v-if="profiles.length === 0">
        Zatím nebyla vložena žádná profilová stránka
      </li>
    </ul>
  </div>
</template>

<script setup lang="ts">
import type { ProfileInfo } from '@/utils/types'

const profiles: ProfileInfo[] = [
  // { name: 'Jan Novák', link: 'jan-novak' }
]
</script>
