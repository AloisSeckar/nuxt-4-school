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
    <div class="p-2 overflow-auto">
      <NuxtPage />
    </div>
    <hr>
    <div class="mt-1 mb-0 text-xs">
      <BackLink />
      <NuxtLink to="/">
        Zpět na úvod
      </NuxtLink>
      ||
      &copy; 2023 - Alois Sečkár
      ||
      <NuxtLink to="https://github.com/AloisSeckar/nuxt-4-school">
        Zdrojový kód projektu
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
