<template>
  <div id="app">
    <h1>Список задач</h1>
    <input 
      v-model="newTodo" 
      @keyup.enter="addTodo" 
      placeholder="Добавить новую задачу"
    >
    <ul>
      <TodoItem
        v-for="(todo, index) in todos"
        :key="index"
        :todo="todo"
        @remove="removeTodo(index)"
      />
    </ul>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue'
import TodoItem from './components/TodoItem.vue'
import { Todo } from './types'

export default defineComponent({
  components: {
    TodoItem
  },
  setup() {
    const newTodo = ref<string>('')
    const todos = ref<Todo[]>([])

    const addTodo = (): void => {
      if (newTodo.value.trim()) {
        todos.value.push({ text: newTodo.value.trim() })
        newTodo.value = ''
      }
    }

    const removeTodo = (index: number): void => {
      todos.value.splice(index, 1)
    }

    return {
      newTodo,
      todos,
      addTodo,
      removeTodo
    }
  }
})
</script>
