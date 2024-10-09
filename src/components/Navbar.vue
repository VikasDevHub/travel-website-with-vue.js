<script setup>
    import { ref } from 'vue';
    import { RouterLink } from 'vue-router';

    const toggle = ref(false)

    const handleToggle = () => {
        toggle.value = !toggle.value
    }

</script>

<template>
    <div class="flex justify-between items-center h-20">
        <RouterLink to="/" class="text-3xl font-semibold">
            BrandName
        </RouterLink>
        <div class="hidden md:flex">
            <RouterLink to="/tours" class="px-4 hover:text-indigo-400">Our tours</RouterLink>
            <RouterLink to="/about" class="px-4 hover:text-indigo-400">About us</RouterLink>
            <RouterLink to="/" class="px-4 hover:text-indigo-400">Booking</RouterLink>
            <RouterLink to="/blogs" class="px-4 hover:text-indigo-400">Blogs</RouterLink>
        </div>
        <div v-if="toggle" class="pt-60 inset-0 z-50 flex flex-col justify-center items-center transition-colors ease-out md:hidden">
            <RouterLink to="/tours" class="pt-4 hover:bg-indigo-400">Our tours</RouterLink>
            <RouterLink to="/about" class="pt-4 hover:text-indigo-400">About us</RouterLink>
            <RouterLink to="/" class="pt-4 hover:text-indigo-400">Booking</RouterLink>
            <RouterLink to="/blogs" class="pt-4 hover:text-indigo-400">Blogs</RouterLink>
        </div>
        <div class="text-3xl hidden md:block"><i class="fa-solid fa-bars"></i></div>
        <div class="text-4xl md:hidden" @click="handleToggle()">&#8801;</div>
    </div>
</template>


<style scoped>
    .cus :hover {
        font-size: 30px;
        color: white;
        background-color: purple;
    }
</style>
