<template>
  <nav class="header">
    <ul>
      <li>
        <a href="#">
          <img src="/favicon.ico" alt="Home" />
          Home
        </a>
      </li>
      <li>
        <a href="#">
          <img src="/favicon.ico" alt="Settings" />
          Settings
        </a>
      </li>
      <li>
        <a href="#">
          <img src="/favicon.ico" alt="Help" />
          Help
        </a>
      </li>
    </ul>
  </nav>
</template>

<script setup lang="ts">
// TypeScript logic for Header, if needed
</script>

<style scoped>
.header {
  background-color: #333;
  color: white;
  height: 100%;
  width: 200px;
  position: fixed;
  top: 0;
  left: 0;
}

.header ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}

.header li {
  padding: 16px;
  text-align: center;
}

.header a {
  color: white;
  text-decoration: none;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.header img {
  width: 24px;
  height: 24px;
}
</style>
