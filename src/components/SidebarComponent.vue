<template>
    <div class="card flex justify-content-center">
        <Sidebar v-model:visible="visible">
            <h2>Sidebar</h2>
             <p-button label="Таблица" icon="pi pi-plus" @click="goToRoute('/cards')" /> 
        </Sidebar>
        <p-button icon="pi pi-search" @click="visible = true" />
    </div>
</template>

<script setup>
import { useRouter } from 'vue-router'
import PButton from 'primevue/button'
import Sidebar from 'primevue/sidebar';
import { ref } from "vue";

const router = useRouter()

function goToRoute(route) {
  router.push(route)
}
const visible = ref(false);
</script>








