<template>
    <div class="w-full border rounded-3xl mt-5" :style="{ height: cardHeight}">
        <div class="relative">
        
             <img :src="imageUrl" alt="card-image" :style="{height: imageHeight}"
             class="w-full rounded-t-xl rounded-b-2xl"/>
            
             <span class="absolute top-2 right-3 glass px-3 text-white rounded-md">
                <i class="fa-regular fa-clock mr-2"></i>
                <slot name="time">
                    9 min read
                </slot>
            </span>
        </div>
        
        <div class="p-4">
            <h1 class="font-semibold my-2">
                <slot name="title">Dummy Title</slot>
            </h1>

            <div class="flex justify-between items-center text-sm">
                <div class="w-4/5"> 
                    <span v-for="(tag, index) in tags" :key="index" class="border px-4 py-1 mr-2 rounded-xl bg-[#f4f4f4]">{{ tag }}</span>
                </div>
                <button class="bg-black text-white rounded-full px-2 w-8 h-8"><i class="fa-solid fa-arrow-right"></i></button>

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
    },
    tags: {
        type: Array,
        default: ["Nature", "Rocks"]
    },
    cardHeight: {
        type: String,
        default: "320px"
    },
    imageHeight: {
        type: String,
        default: "224px"
    }
});
</script>

<style scoped>

</style>