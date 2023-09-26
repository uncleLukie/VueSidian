<!-- pages/[...slug].vue -->
<template>
  <div class="page">
    <PostList />
    <ContentDoc />
  </div>
</template>

<script setup lang="ts">
import PostList from '~/components/PostList.vue'
</script>

<style scoped>
.page {
  /* Page styles */
}
</style>
