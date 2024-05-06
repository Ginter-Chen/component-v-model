<script setup lang="ts">
// import { ref } from 'vue'

defineProps<{ msg: string }>()

const count = defineModel('count',{default: 0})
const input = defineModel('input',{default: ""})
</script>

<template>
  <h1>{{ msg }}</h1>

  <div class="card">
    <button type="button" @click="count++">Child count is {{ count }}</button>
    <br>
    <br>
    <input type="text" v-model="input">
  </div>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
