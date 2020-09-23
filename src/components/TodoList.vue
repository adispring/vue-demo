<template>
  <div class="ToDoList">
    <h1 v-html="title">My TodoList</h1>
  </div>
</template>

<script>
  export default {
    name: 'ToDoList',
    data() {
      return {
        title: '<span></span> this is a todo list',
      };
    },
  };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h3 {
    margin: 40px 0 0;
  }
  ul {
    list-style-type: none;
    padding: 0;
  }
  li {
    display: inline-block;
    margin: 0 10px;
  }
  a {
    color: #42b983;
  }
</style>
