<template>
    <div class="h-80 w-72 border rounded-2xl mt-5">
        <div class="relative">
        
             <img :src="imageUrl" alt="card-image" 
             class="max-h-60 w-full rounded-t-xl rounded-b-2xl"/>
            
             <span class="absolute top-2 right-3 glass px-3 text-white rounded-md">5.0 <i class="fa-solid fa-star"></i></span>
        </div>
        
        <div class="p-3">
            <h1 class="font-semibold my-2">
                <slot name="title">Alone with nature</slot>
            </h1>

            <div class="flex justify-between items-center text-sm">
                
                <p> <span class="font-semibold"><slot name="price">$100</slot></span>/ person </p>
                <button class="bg-black text-white rounded-full w-7 h-7 px-2"><i class="fa-solid fa-arrow-right"></i></button>
            </div>
        </div>
    </div>
</template>

<script setup>
import { defineProps } from 'vue';

const props = defineProps({
    imageUrl: {
        type: String,
        default: 'https://dynamic-media-cdn.tripadvisor.com/media/photo-o/27/f3/b7/11/caption.jpg?w=500&h=400&s=1'
    }
});
</script>

<style scoped>

</style>