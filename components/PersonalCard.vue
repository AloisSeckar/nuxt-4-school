<template>
  <div class="px-4 pb-4 border-2 rounded-xl" :style="`background-color: ${background}`">
    <h2 class="text-center">
      {{ fullName }}
    </h2>
    <img :src="image" class="w-32 m-auto border-2 border-black rounded-full">
    <div class="text-center font-bold mb-2">
      {{ age }} let, {{ place }}
    </div>
    <div class="text-center">
      {{ about }}
    </div>
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
  about: { type: String, default: 'Něco o mě' },
  background: { type: String, default: 'rgb(236 253 245)' }
})

const fullName = `${props.firstName} ${props.lastName}`
</script>
