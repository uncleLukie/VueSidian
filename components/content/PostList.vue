<template>
  <ul>
    <li v-for="post in posts" :key="post.slug">
      <nuxt-link :to="`/${post.slug}`" @click.native="setCurrentPath(post.slug)">
        {{ post.title }}
      </nuxt-link>
    </li>
  </ul>
</template>

<script setup lang="ts">
import { inject } from 'vue'
import { useAsyncData } from '#app'
import type { ProvideProps } from '@/types.d.ts'

// Use inject method here with a non-null assertion
const injectedProps = inject<ProvideProps>('setCurrentPath')
if (!injectedProps) {
  throw new Error('setCurrentPath not provided')
}
const { setCurrentPath } = injectedProps

// queryContent should be available globally
const { data: posts } = useAsyncData('posts-list', () => queryContent('/').find())
</script>
