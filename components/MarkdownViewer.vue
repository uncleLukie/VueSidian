<script setup>
import { ref } from 'vue'
import { queryContent } from '@nuxt/content'

const markdownData = ref(null)

// Fetch content
queryContent('/some-markdown-path').fetch().then(response => {
  markdownData.value = response
})
</script>

<template>
  <ContentRenderer :value="markdownData" />
</template>
