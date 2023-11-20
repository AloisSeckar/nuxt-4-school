<template>
  <div>
    <h2>VOŠ AHOL, Ostrava - 20.11.2023</h2>
    <div>
      Výsledky workshopu:
    </div>
    <ul class="list-disc pl-6">
      <li v-for="item in profiles" :key="item.link">
        <NuxtLink :to="`/2023/ahol/${item.link}`">
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
  { name: 'Honzík Pomásle', link: 'honzik-pomasle' },
  { name: 'Petr Novák', link: 'petr-novak' },
  { name: 'Andrea Durčáková', link: 'andrea-durcakova' },
  { name: 'David Matyáš', link: 'david-matyas' },
  { name: 'Sebastian Lička', link: 'sebastian-licka' }
]
</script>
