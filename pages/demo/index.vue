<template>
  <div>
    <h2>DEMO HODINA, 01.11.2023, Internet</h2>
    <div>
      Toto je ukázková podoba výsledné stránky na konci workshopu. Nachází se zde seznam s odkazy na
      stránky vytvořené jednotlivými účastníky.
    </div>
    <ul class="list-disc pl-6">
      <li v-for="item in profiles" :key="item.link">
        <NuxtLink :to="`/demo/${item.link}`">
          <strong>{{ item.name }}</strong>
        </NuxtLink>
      </li>
    </ul>
  </div>
</template>

<script setup lang="ts">
const profiles = [
  { name: 'Jan Novák', link: 'jan-novak' },
  { name: 'Alois Sečkár', link: 'alois-seckar' }
]
</script>
