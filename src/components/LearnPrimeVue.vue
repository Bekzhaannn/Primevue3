<template>
  <div class="card">
    <PDataTable :value="data">
      <PColumn v-for="column in columns" :key="column.field" :field="column.field" :header="column.header" />
    </PDataTable>
  </div> 

  <PInputText v-model="search"/>


</template>


<script setup>
import { ref, onMounted } from 'vue'
import PDataTable from 'primevue/datatable'
import PColumn from 'primevue/column'
import PInputText from 'primevue/inputtext'

const search = ref ('')

const data = [
  {
    id: 1,
    name: 'BMW',
    price: 10000,
  },
  {
    id: 2,
    name: 'Audi',
    price: 12000,
  },
  {
    id: 3,
    name: 'Mercedes',
    price: 15000,
  },
]

const columns = [
  {
    field: 'id',
    header: 'ID',
  },
  {
    field: 'name',
    header: 'Название',
  },
  {
    field: 'price',
    header: 'Цена',
  },
]
</script>

