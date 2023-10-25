<template>
  <div class="text-center">
    <h2>{{ fullName }}</h2>
    <img :src="image" class="w-32 m-auto">
    <div>{{ age }}</div>
    <div>{{ place }}</div>
    <div>{{ about }}</div>
  </div>
</template>

<script setup lang="ts">
const props = defineProps({
  // TODO required prop align of certain type
  firstName: { type: String, default: 'Jméno' },
  lastName: { type: String, default: 'Příjmení' },
  image: { type: String, default: '/profile.png' },
  age: { type: Number, default: 99 },
  place: { type: String, default: 'Odkud jsem' },
  about: { type: String, default: 'Něco o mě' }
})

const fullName = `${props.firstName} ${props.lastName}`
</script>
