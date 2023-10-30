<template>
  <div v-if="backlink" class="inline">
    <NuxtLink :to="backlink">
      Zpět
    </NuxtLink>
    ||
  </div>
</template>

<script setup lang="ts">
const path = computed(() => useRoute().path)
const backlink = computed(() => path.value.substring(0, path.value.lastIndexOf('/')))
</script>
