<script setup lang="ts">
import { ref, Ref } from 'vue'
import TodoAddForm from './TodoAddForm.vue'
import TodoList from './TodoList.vue'
  export type Todo = {
    id: number,
    content: string,
    isDone: boolean
  }

  const todos: Ref<Todo[]> = ref([
    {id: 1, content: 'Study Vue3', isDone: true},
    {id: 2, content: 'Study TypeScript', isDone: true},
    {id: 3, content: 'Study Java', isDone: false},
  ])
</script>

<template>
  <div class="myTodo">My Todos</div>
  <TodoAddForm />
  <TodoList :todos="todos" />
</template>

<style scoped>
  .myTodo {
    text-align: center;
    align-content: center;
  }
</style>