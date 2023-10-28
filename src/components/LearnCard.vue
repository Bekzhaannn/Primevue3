<template>
<template v-for="burger in burgers" :key="burger.title">
    <card style="width: 20rem">
      <template #header>
        <template v-if="burger.title.includes('БУРГЕР')">
          <img alt="Бургер" src="https://primefaces.org/primevue/showcase/images/demo/product/cheeseburger.jpg" />
        </template>
        <template v-else>
          <img alt="РОЛЛ" src="https://primefaces.org/primevue/showcase/images/demo/product/baconburger.jpg" />
        </template>
        <template v-if="burger.description.includes('')">
                <div class="card flex flex-wrap gap-2">
                    <Chip label="ПП еда" />
                </div>
        </template>
        <template v-else>
          <div class="card flex flex-wrap gap-2">
                    <Chip label="Вредная еда" />
                </div>
        </template>
        <template v-if="burger.description.includes('стрипса')">
                <div class="card flex flex-wrap gap-2">
                    <Chip label="Курица" />
                </div>
        </template>
        <template v-else>
          <div class="card flex flex-wrap gap-2">
                    <Chip label="Говядина" />
                </div>
        </template>
      </template>
      <template #title> {{ burger.title }} </template>
      <template #content>{{ burger.description }}</template>
    </card>
</template>

</template>


<script setup>
import Card from 'primevue/card';
import Chip from 'primevue/chip';

const burgers =[{
    title: "САНДЕРС МЕГА БУРГЕР", description:'3 стрипса, томаты, салат айсберг, соленые огурчики, соус Бургер Классик, булочка бриошь и 2 ломтика сыра', imageSrc: 'https://www.google.com/url?sa=i&url=https%3A%2F%2Fdepositphotos.com%2Fru%2Fphotos%2F%25D0%25B1%25D1%2583%25D1%2580%25D0%25B3%25D0%25B5%25D1%2580.html&psig=AOvVaw2ZRgy-Dj5MRONgWf3U_DEA&ust=1697948984813000&source=images&cd=vfe&ved=0CBEQjRxqFwoTCLCjyYKnhoIDFQAAAAAdAAAAABAE'},
{ title: "Айтвистер", description:'филе, салат айсберг, маринованные огурцы, лук, соус Бургер на пшеничной булочке', imageSrc: 'https://www.google.com/url?sa=i&url=https%3A%2F%2Fdepositphotos.com%2Fru%2Fphotos%2F%25D0%25B1%25D1%2583%25D1%2580%25D0%25B3%25D0%25B5%25D1%2580.html&psig=AOvVaw2ZRgy-Dj5MRONgWf3U_DEA&ust=1697948984813000&source=images&cd=vfe&ved=0CBEQjRxqFwoTCLCjyYKnhoIDFQAAAAAdAAAAABAE'}
]
</script>

<style scoped>
.card {
    margin: 5px;
}

</style>