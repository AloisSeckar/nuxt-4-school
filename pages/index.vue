<template>
  <div>
    <div>
      V rámci projektu <a href="https://www.denproskolu.cz/">Den pro školu</a>
      nabízím IT workshopy na téma <strong>"Vývoj webových aplikací pomocí frameworku Nuxt"</strong>.
      Jsou určeny spíše pro pokročilejší studenty informatiky.
      Pro žáky, kteří s programováním teprve začínají, je vhodnější workshop
      <a href="https://web-4-school.netlify.app/">"Základy tvorby webových stránek"</a>.
    </div>
    <h2>POPIS WORKSHOPU</h2>
    <div>
      Studenti se seznámí s frameworkem <a href="https://nuxt.com/">Nuxt</a> určeným pro tvorbu webových
      aplikací v programovacím jazyce JavaScript. Výklad bude probíhat názorně nad zdrojovým kódem tohoto projektu,
      který je veřejně k dispozici <a href="https://github.com/AloisSeckar/nuxt-4-school">ZDE</a>.
      Součástí bude též seznámení se (a výklad, bude-li třeba), jak funguje verzovácí systém
      <a href="https://git-scm.com/">Git</a> a odvozená platforma <a href="https://github.com/">GitHub</a>
      a jak tyto nástroje umožňují souběžnou práci více programátorů.
    </div>
    <div>
      Cílem workshopu bude vytvoření osobní stránky každého účastníka, která bude v průběhu výuky přidána
      do tohoto projektu a stane se jeho veřejnou součástí. Součástí procesu je tedy nejen samotný vývoj
      pomocí Nuxt, ale i vyzkoušení si vzájemné kolaborace v rámci většího projektu (všichni budou pracovat
      nad společným zdrojovým kódem). Zájemci budou mít do projektu možnost vstupovat i v budoucnu
      a své příspěvky dále vylepšovat.
    </div>
    <div>
      Pro představu viz
      <NuxtLink to="/demo">
        DEMO APLIKACE
      </NuxtLink>
    </div>
    <h2>PŘEDPOKLADY WORKSHOPU</h2>
    <div>
      Základní znalost HTML, CSS a JavaScriptu, nebo alespoň základní orientace v problematice programování
      a schopnost zorientovat se v nové technologii na základě praktického výkladu přímo během workshopu.
    </div>
    <div>
      Je třeba mít nainstalováno nebo mít možnost v rámci projektu nainstalovat následující aplikace:
    </div>
    <ul class="list-disc pl-6">
      <li>
        <strong>Git</strong> - verzovací software pro kolaborativný vývoj aplikací (<a href="https://git-scm.com/">https://git-scm.com/</a>)
      </li>
      <li>
        <strong>VS Code</strong> - integrované vývojové prostředí pro programování (<a href="https://code.visualstudio.com/">https://code.visualstudio.com/</a>)
      </li>
      <li>
        <strong>Node.js</strong> - lokální běhové prostředí pro JavaScriptové aplikace (<a href="https://nodejs.org/">https://nodejs.org/</a>)
      </li>
    </ul>
    <h2>ROZCESTNÍK PROJEKTŮ</h2>
    <div>
      Zde naleznete odkazy na jednotlivé proběhlé workshopy a osobní stránky jednotlivých studentů
      vytvořené během proběhlých projektů.
    </div>
    <ul class="list-disc pl-6">
      <li v-for="item in events" :key="item.link">
        <strong>{{ item.date }}</strong>
        -
        <NuxtLink :to="item.link">
          {{ item.name }}
        </NuxtLink>
      </li>
    </ul>
  </div>
</template>

<script setup lang="ts">
import type { EventInfo } from '@/utils/types'

const events: EventInfo[] = [
  { date: '20.11.2023', name: 'VOŠ AHOL, Ostrava', link: '/2023/ahol' }
]
</script>
