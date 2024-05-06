<script setup lang="ts">
import { ref } from 'vue'
import Child from './components/child.vue'

const count  = ref(0);
const input = ref("default");
</script>

<template>
  <div>
    <a href="https://vitejs.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>
  <h1>Parent</h1>
  <p>Parent count is {{ count }}</p>
  <p>Parent string is {{ input }}</p>
  <Child msg="Child" v-model:count="count" v-model:input="input"/>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
