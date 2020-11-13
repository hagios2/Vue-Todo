<template>
  <div>
    <div v-for="todo in todos" v-bind:key="todo.id">
      <TodoItem v-bind:todo_item="todo" v-on:del-todo="$emit('del-todo', todo.id)"></TodoItem>
    </div>
  </div>
</template>

<script>
import TodoItem from "@/views/TodoItem";
export default {
  name: "Todos",
  props: ["todos"],
  components: {
    TodoItem
  }
}
</script>
<style scoped>


</style>