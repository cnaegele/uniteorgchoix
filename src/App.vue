<template>
  <v-app>
    <v-main>
      <Suspense><UniteOrgChoix uniteHorsVdL="non" modeChoix="unique"/></Suspense>
    </v-main>
  </v-app>
</template>

<script setup>
import UniteOrgChoix from './components/UniteOrgChoix.vue';
</script>
