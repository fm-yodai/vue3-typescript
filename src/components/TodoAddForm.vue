<script setup lang="ts">
  import { ref } from 'vue'

  let newTodo = ref<string>("")
</script>

<template>
  <div>
    <input v-model="newTodo" placeholder="Add new Todo" />
  </div>

</template>

<style scoped>

</style>