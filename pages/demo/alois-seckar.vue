<template>
  <div class="flex">
    <div class="m-1 w-64">
      <PersonalCard
        first-name="Alois"
        last-name="Sečkár"
        image="/seckar.jpg"
        :age="getAge()"
        place="Praha"
        :about="about"
        background="cornsilk"
      />
    </div>
    <div class="m-1 px-4 pb-4 w-full border-2 rounded-xl overflow-auto">
      <h2>Osobní text</h2>
      <div class="text-justify">
        Anwa almiel coivië taniquelassë laurië wendë lanyë formaitë wë tosta cundu.
        Vet yór asanótë incë. Corima tulunca hácala yúyo atya andúnë usta ingaran termar.
        ávë vëo moia ces ëala oloirë nyë hyarma vaita tya ambarussa nólion sermo tamin
        quendendil úamanyar lunca nyenna sisíla. Valima apsene sindië pilin perian nandin.
        Láma calwa notessë rista toron uru lumba eldanor. Orocarni línen melin lumbulë sú.
        Horya lapsa vó roimë lantalca stë aian mirwa elerína nyel hísilanya sulpa cormë laurëa.
        Luvu wil inqua olofantur hyarma cenda úrimë rúcarë táva. Melehta cópa lúcë qualin tier.
        Nelcë taimë cainen ataformo úa tes.
      </div>
    </div>
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
