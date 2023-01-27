<script setup lang="ts">
  import { Todo } from './TodoApp.vue'

  defineProps<{
    todos: Todo[]
  }>()

</script>

<template>
  <div v-if="!todos.length">No Todo Here</div>
  <div v-else>
    <ul>
      <li v-for="todo in todos" :key="todo.id">
        <input v-model="todo.isDone" type="checkbox"/>
        <span :class="{ 'todo-done': todo.isDone }">{{ todo.content }}</span>
      </li>
    </ul>
  </div>

</template>

<style scoped>
  ul {
    list-style: none;
  }
  ul li {
    position: relative;
    text-align: left;
  }
  .todo-done {
    text-decoration: line-through;
  }
</style>