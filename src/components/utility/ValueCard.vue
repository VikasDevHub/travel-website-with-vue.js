<template>
    <div class="flex flex-col justify-center items-center h-80 w-72 p-5">
        <div class="p-3 bg-gray-200 rounded-full">
            <slot name="icon">
                <i class="fa-solid fa-paper-plane"></i>
            </slot>
        </div>
        
        <h1 class="text-xl font-semibold my-2">
            <slot name="title">Airport Pickup</slot>
        </h1>

        <p class="text-center text-sm">
            <slot name="content">We Provide escort from the airport to the hotel</slot>
        </p>
    </div>
</template>

<script setup>
import { defineProps } from 'vue';

const props = defineProps()

</script>