<template>
  <li>
    <span>{{ todo.text }}</span>
    <button class="delete-btn" @click="$emit('remove')">Удалить</button>
  </li>
</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue'
import { Todo } from '../types'

export default defineComponent({
  props: {
    todo: {
      type: Object as PropType<Todo>,
      required: true
    }
  }
})
</script>
