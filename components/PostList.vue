<script setup>
import { ref } from 'vue'
import { queryContent } from '@nuxt/content'

const posts = ref([])

// Fetch content
queryContent('blog').fetch().then(response => {
  posts.value = response
})
</script>

<template>
  <ul>
    <li v-for="post in posts" :key="post.slug">
      {{ post.title }} - {{ post.date }}
    </li>
  </ul>
</template>
