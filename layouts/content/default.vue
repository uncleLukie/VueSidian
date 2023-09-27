<template>
  <div class="content-layout">
    <slot name="sidebar"></slot>
    <slot></slot>
  </div>
</template>

<style scoped>
.content-layout {
  display: flex;
}
</style>
