<template>
  <div id="app">
    <div class="container">
      <addTodo/>
      <filterTodos/>
      <Todos/>
    </div>
  </div>
</template>

<script>
import Todos from './components/Todos.vue'
import addTodo from './components/addTodo.vue'
import filterTodos from './components/filterTodos.vue'

export default {
  name: 'App',
  components: {
    Todos,
    addTodo,
    filterTodos
  }
}
</script>

<style>
body {
  font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
  line-height: 1.6;
  background: #e8f7f0;
}
.container {
  max-width: 1100px;
  margin: auto;
  overflow: auto;
  padding: 0 2rem;
}
</style>
