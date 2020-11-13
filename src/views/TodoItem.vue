<template>
  <div  class="todo-item" :class="{'is-completed': todo_item.completed}">
    <input type="checkbox" @change="markComplete">
    <p >{{todo_item.title}}
      <button @click="$emit('del-todo', todo_item.id)" class="del">X</button>
    </p>
  </div>
</template>

<script>
export default {
  name: "TodoItem",
  props: ['todo_item'],
  methods: {
    markComplete(){
      this.todo_item.completed = ! this.todo_item.completed
    }
  }
}
</script>

<style scoped>

.todo-item {
  background: #f4f4f4;
  padding: 10px;
  border-bottom: 1px #ccc dotted;
}
.is-completed {
  text-decoration: line-through;
}
.del {
  background: #ff0000;
  color: #fff;
  border: none;
  padding: 5px 9px;
  border-radius: 50%;
  cursor: pointer;
  float: right;
}

</style>