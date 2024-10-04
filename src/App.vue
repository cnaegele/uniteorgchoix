<template>
  <v-app>
    <v-main>
      <Suspense>
        <UniteOrgChoix 
          uniteHorsVdL="non" 
          modeChoix="multiple"
          @choixUniteOrg="receptionUniteOrg"
        />
      </Suspense>
    </v-main>
  </v-app>
</template>

<script setup>
import UniteOrgChoix from './components/UniteOrgChoix.vue';

const receptionUniteOrg = (jsonData) => {
  console.log(`Réception unité organisationnelle \njson: ${jsonData}`)
  if (window.opener && typeof window.opener.receptionUniteOrg24 === 'function') {
    window.opener.receptionUniteOrg24(jsonData)
  }
}
</script>
