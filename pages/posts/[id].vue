<script setup>
const route = useRoute()

const { data: post } = await useFetch(`https://jsonplaceholder.typicode.com/posts/${route.params.id}`)
</script>

<template>
  <h1 class="text-3xl font-bold">{{ post.title }}</h1>
  <p class="mt-6">{{ post.body }}</p>
</template>
