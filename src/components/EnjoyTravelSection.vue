<template>
    <div class="py-10">
        <div class="max-h-full relative">
            <img :src="imageUrl" :alt=alt class="image-class" />
            <div class="text-white absolute top-20 left-20 z-10">
                <h1 class="text-6xl font-semibold">Enjoy your <br>travel</h1>
                <p class="mt-6 font-semibold">
                    Discover the most unique and vibrant <br>
                    experience the Azores have to offer
                </p>
            </div>
            <div id="lighthouse"
                class="absolute right-36 top-20 w-1/3 h-80 flex justify-center items-center border rounded-xl border-white">
            </div>
            <div class="glass absolute right-[479px] top-24 text-white px-3 py-2 text-sm">Lighthouse Forol <br> Ponto do Arnel</div>
        </div>
    </div>
</template>

<script setup>

const props = defineProps({
    imageUrl: {
        type: String,
        default: 'https://media01.stockfood.com/largepreviews/MjIwNDkyMzc5NA==/71126574-Ponta-do-Arnel-lighthouse-Sao-Miguel-Azores-Portugal.jpg'
    },
    alt: {
        type: String,
        default: "enjoy-travel-image"
    }
});
</script>

<style scoped>
.image-class {
    width: 100%;
    /* Full width of the container */
    height: auto;
    /* Maintain aspect ratio */
    max-height: 600px;
    /* Maximum height */
    min-height: 400px;
    /* Minimum height */
    object-fit: cover;
    /* Ensure the image covers the element area */
}
.glass {
    background: rgba(255, 255, 255, 0.2);
    border-radius: 16px;
    box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
    backdrop-filter: blur(5px);
    -webkit-backdrop-filter: blur(5px);
    border: 1px solid rgba(255, 255, 255, 0.3);
    }
</style>