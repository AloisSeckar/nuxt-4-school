<template>
  <div>
    <PersonalCard
      first-name="Alois"
      last-name="Sečkár"
      :age="getAge()"
      place="Praha"
      :about="about"
    />
  </div>
</template>

<script setup lang="ts">
const getAge = () => {
  const birthday = new Date('1988-07-21')
  const today = new Date()
  let age = today.getFullYear() - birthday.getFullYear()
  if (today.getMonth() < birthday.getMonth() ||
    (today.getMonth() === birthday.getMonth() && today.getDate() < birthday.getDate())) {
    age--
  }
  return age
}

type Quote = {
    id: number,
    quote: string,
    author: string
}

let about: string
const id = Math.floor(Math.random() * 100) + 1
const { data } = await useFetch<Quote>(`https://dummyjson.com/quotes/${id}`)
if (data.value) {
  about = `${data.value.quote} - ${data.value.author}`
} else {
  about = 'fetch failed'
}
</script>
