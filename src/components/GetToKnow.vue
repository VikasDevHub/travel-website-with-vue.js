<script setup>
import BookNowBtn from './utility/BookNowBtn.vue';
</script>

<template>
    <div class="my-10">
        <div class="relative">
            <img src="https://plus.unsplash.com/premium_photo-1669297900794-fe4c57a3306d?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MTN8fG1vdW50YWlucyUyMHN1bnNldHxlbnwwfHwwfHx8MA%3D%3D" 
            alt="" class="w-full h-[500px] rounded-2xl">
            <div class="absolute top-28 left-1/4">
                <div class="mb-10 text-4xl md:text-5xl lg:text-7xl text-white tracking-wide font-semibold">Let's get to know <br> the Azores</div>
                <div class="lg:text-center text-start"><BookNowBtn/></div>
            </div>
        </div>
    </div>
</template>