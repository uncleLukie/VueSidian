<template>
  <ContentRenderer :value="markdownData" />
</template>

<script setup lang="ts">
import { defineProps } from 'vue'
import { useAsyncData } from '#app'

const { path } = defineProps(['path'])
const { data: markdownData } = useAsyncData('markdown-viewer', () => queryContent(path).findOne())
</script>
