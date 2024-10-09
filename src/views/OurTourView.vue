<script setup>
    import { ref } from 'vue'
    import tours from '../data/tours.js';
    import TourCard from '@/components/utility/TourCard.vue';
    

    const toursData = ref(tours)
    
</script>
<template>
    <div class="container py-10 h-full">
        <h1 class="text-center text-5xl my-10">Our Tours</h1>
        <div>
            <div v-if="tours.length > 0">
                <div class="grid grid-cols-1 md:grid-cols-2 md:gap-4 lg:grid-cols-4 lg:gap-1">
                    <TourCard v-for="(tour, index) in toursData" :key="index" :image-url="tour.imageUrl" class="mx-auto">
                        <template #title>{{ tour.title }}</template>
                        <template #price>{{  tour.price }}</template>
                    </TourCard>
                </div>
            </div>

            <div v-else class="text-center my-10">
                No Records are found !
            </div>
        </div>
    </div>
</template>