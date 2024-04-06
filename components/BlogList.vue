<template>
    <div class="blog-container">
        <div :for="post in posts.data" :key="post.id">
            <img class="post-img" :src="post.attributes.image.data.attributes.url" :alt="post.attributes.title">
            <h2>{{  post.attributes.title }}</h2>
            <p>{{  post.attributes.summary }}</p>
        </div>
    </div>
</template>

<script setup>
    defineProps({
        posts: Object
    })
</script>

<style>
    .blog-container {
        display: flex;
        gap: 2rem;
    }

    .post-img {
        border-radius: 5px;
    }
</style>