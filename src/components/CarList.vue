<script setup>
import CarItem from '@/components/CarItem.vue'
import { onMounted } from 'vue'
import { useAuto } from '../composable/useAuto'
import { useRouter } from 'vue-router'

const router = useRouter()
const { autoListRemake, getAutoList } = useAuto()

onMounted(async () => {
  await getAutoList()
})

function goToCarUrl(id) {
  router.push({ name: 'car', params: { id } })
}
</script>

<template>
  <div class="car_info">
    <section class="cars" v-for="auto in autoListRemake" :key="auto">
      <CarItem :auto="auto" @click.stop="goToCarUrl(auto.id)" :price="auto.price" />
    </section>
  </div>
</template>

<style scoped>
:deep(.p-card) {
  transform: perspective(1000px) !important;
  position: relative !important;
}

:deep(.p-card):hover {
  animation: transform 1s ease-in-out !important;
  cursor: pointer;
  transform: scale(1.1) !important;
}

@keyframes transform {
  0% {
    transform: rotateY(0deg);
  }
  50% {
    transform: rotateY(180deg);
  }
  100% {
    transform: rotateY(360deg);
  }
}
.car_info {
  width: 1170px;
  margin: 0 auto;
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
  padding-inline: 50px;
  text-align: center;
}

.cars {
  margin-bottom: 10px;
  margin-top: 10px;
}
</style>


<template>
    <div class="card">
        <DataTable :value="products" tableStyle="min-width: 50rem">
            <Column field="code" header="Code" sortable style="width: 25%"></Column>
            <Column field="name" header="Name" sortable style="width: 25%"></Column>
            <Column field="category" header="Category" sortable style="width: 25%"></Column>
            <Column field="quantity" header="Quantity" sortable style="width: 25%"></Column>
        </DataTable>
    </div>
</template>

<script setup>
import { ref, onMounted } from 'vue';
import { ProductService } from '@/service/ProductService';

onMounted(() => {
    ProductService.getProductsMini().then((data) => (products.value = data));
});

const products = ref();

</script>