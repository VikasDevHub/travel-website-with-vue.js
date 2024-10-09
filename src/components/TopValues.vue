<script setup>
import ValueCard from './utility/ValueCard.vue';
import TourCard from './utility/TourCard.vue';
import Button from './utility/Button.vue';
import tours from '../data/tours.js'
import { ref } from 'vue';

const data = ref([
    {icon: "fa-solid fa-paper-plane", title: "Airport Pickup", content: "We Provide escort from the airport to the hotel"},
    {icon: "fa-solid fa-wallet", title: "Easy booking", content: "Quick and easy booking of tours for upcoming dates"},
    {icon: "fa-solid fa-users-line", title: "Best tour guide", content: "Our best tour guide is ready to guide your trip"},
    {icon: "fa-brands fa-skyatlas", title: "Lots of promos", content: "Various promotion and drawing of tours"},
])

const toursData = ref(tours)

</script>
<template>
    <div class="py-5">
        <div class="text-center">
            <h1 class="text-5xl mt-10">Top Values For You</h1>
            <p class="mt-4">Try variety of benifits when using our service</p>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 lg:gap-1">
            <ValueCard v-for="(val, index) in data" :key="index" class="mx-auto">
                <template #icon>
                <i :class="val.icon"></i>
                </template>
                <template #title>
                   {{ val.title }}
                </template>
                <template #content>
                    {{  val.content }}
                </template>
            </ValueCard>
        </div>
        <div id="choose-tour">
            <h1 class="text-5xl">Choose your tour</h1>
            <div class="mt-10 grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 lg:gap-1">
                <TourCard v-for="(tour, index) in toursData" :key="index" :image-url="tour.imageUrl" class="mx-auto">
                    <template #title>{{ tour.title }}</template>
                    <template #price>{{  tour.price }}</template>
                </TourCard>
            </div>
            <div class="text-center mt-10">
                <RouterLink to="/tours">
                    <Button>
                        See all
                    </Button>
                </RouterLink>
            </div>
        </div>
    </div>

</template>


<style scoped>
   
</style>
