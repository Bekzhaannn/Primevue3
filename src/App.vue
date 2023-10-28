<script setup>
import { RouterView } from 'vue-router'
// import NavBar from '@/components/layouts/NavBar.vue'
// import LearnPrimeVue from './components/LearnPrimeVue.vue'
// import Myfile from './components/Myfile.vue'
// import Toolip from './components/Toolip.vue'
// import LearnCard from './components/LearnCard.vue'
// import OrganizationChart from './components/OrganizationChart.vue'
import SidebarComponent from './components/SidebarComponent.vue'

</script>

<template>
  <!-- <NavBar /> -->
  <SidebarComponent/>
  <!-- <LearnPrimeVue />  -->
  <!-- <LearnCard/> -->
  <!-- <OrganizationChart/> -->
  <!-- <Myfile/> -->
  <!-- <Toolip/> -->
  <router-view />
</template>

<style scoped></style>


