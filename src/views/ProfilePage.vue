
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

<script setup></script>
