<template>
    <div class="card overflow-x-auto">
        <OrganizationChart :value="data">
            <template #default="slotProps">
                <span>{{ slotProps.node.label }}</span>
            </template>
        </OrganizationChart>
    </div>
</template>

<script setup>
import OrganizationChart from 'primevue/organizationchart';

import { ref } from "vue";

const data = ref({
    label: 'МЕНЮ',
    children: [
        {
            label: 'ШЕФ БУРГЕР',
            children: [
                {
                    label: 'БУЛКА'
                },
                {
                    label: 'КОТЛЕТА'
                }
            ]
        },
        {
            label: 'РОЛЛ',
            children: [
                {
                    label: 'ЛАВАШ'
                },
                {
                    label: 'МЯСО'
                }
            ]
        }
    ]
});
</script>