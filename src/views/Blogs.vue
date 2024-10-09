<script setup>
    import { ref } from 'vue'
    import blogs from '../data/blogs.js';
    import BlogCard from '@/components/utility/BlogCard.vue';

    const blogsApi = ref(blogs)
    
</script>
<template>
    <div class="container py-10 h-full">
        <h1 class="text-center text-5xl my-10">Blog Page</h1>
        <div>
            <div v-if="blogsApi.length > 0">
                <div class="grid grid-cols-1 mt-5 md:grid-cols-2 md:gap-6">
                    <BlogCard v-for="(blog, index) in blogsApi" :key="index" :imageUrl="blog.imageUrl"
                        :tags="blog.tags">
                        <template #time>{{  blog.time }}</template>
                        <template #title>{{ blog.title }}</template>
                    </BlogCard>
                </div>
            </div>

            <div v-else class="text-center my-10">
                No Blogs are posted yet!
            </div>
        </div>
    </div>
</template>