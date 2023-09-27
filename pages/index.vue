<script setup lang="ts">
import { ref, provide } from 'vue'
import type { ProvideProps } from '@/types.d.ts'

const currentPath = ref('')

const setCurrentPath = (path: string) => {
  currentPath.value = path
}

// Create an object that matches ProvideProps interface
const provideProps: ProvideProps = {
  setCurrentPath
}

// Use provide here
provide('setCurrentPath', provideProps)
</script>

<template>
  <div class="page">
    <PostList />
    <MarkdownViewer :path="currentPath" />
  </div>
</template>
