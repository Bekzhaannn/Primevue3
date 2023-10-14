<script setup>
import { RouterView } from 'vue-router'
import NavBar from '@/components/layouts/NavBar.vue'
import LearnPrimeVue from './components/LearnPrimeVue.vue'
</script>

<template>
  <NavBar />
  <LearnPrimeVue />
  <router-view />
</template>

<style scoped></style>
