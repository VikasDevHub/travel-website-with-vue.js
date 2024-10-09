<template>
    <div class="py-5">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
            <div class="text-5xl">Blog about <br> traveling</div>
            <div class="p-2">
                <div class="">The most exoctic island in Europe in the center of vast blue
                    ocean, enveloped by a mild martime climate and the br
                    paradisical beauty of untouched nature imaginable
                    Lorem ipsum dolor sit amet.
                </div>
                <div class="mt-7">
                    <RouterLink to="/blogs"><Button>Read all articles</Button></RouterLink>
                </div>
            </div>
        </div>

        <div>

            <div class="grid grid-cols-1 gap-6 md:grid-cols-2">
                <BlogCard cardHeight="660px" imageHeight="560px" imageUrl="https://media.istockphoto.com/id/868927110/photo/waterfalls-on-flores-island-azores-portugal.jpg?s=612x612&w=0&k=20&c=cdPpqfndrHAAan70Iip-xbEwGq3VMjAggvOby91DBBM="/>
                <div class="grid grid-cols-1">
                    <BlogCard/>
                    <BlogCard/>
                </div>
            </div>

            
        </div>


    </div>
</template>

<script setup>
import Button from './utility/Button.vue';
import BlogCard from './utility/BlogCard.vue';
import blogs from '../data/blogs.js';
import { ref } from 'vue';

const blogsApi = ref(blogs)
// console.log(blogsApi.value)
</script>