<template>
  <div class="m-1 p-1">
    <h1 class="text-3xl text-emerald-600 font-bold">
      <NuxtLink to="/">
        nuxt-4-school
      </NuxtLink>
    </h1>
    <div class="mb-1">
      Základy vývoje webových stránek ve frameworku Nuxt
    </div>
    <hr>
    <div class="m-2 p-2 border-2 overflow-auto">
      <NuxtPage />
    </div>
    <hr>
    <div class="mt-1 text-xs">
      <NuxtLink to="https://github.com/AloisSeckar/nuxt-4-school" class="text-emerald-600 hover:text-emerald-400">
        https://github.com/AloisSeckar/nuxt-4-school
      </NuxtLink>
    </div>
  </div>
</template>

<script setup lang="ts">
useHead({
  title: 'nuxt-4-school',
  htmlAttrs: {
    lang: 'cs'
  }
})
</script>
