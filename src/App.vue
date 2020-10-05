<template>
  <div id="app">
    <SlotTodoList
      :filteredTodos="filteredTodos"
      :toggle="toggleTodo"
    ></SlotTodoList>
  </div>
</template>

<script type="text/babel">
import SlotTodoList from './components/SlotTodoList.vue';

export default {
  name: 'App',
  components: {
    SlotTodoList,
  },
  data() {
    return {
      baseName: 'default',
      user: {
        name: 'adi',
      },
      todoList: [
        {
          id: 1,
          text: '学习 vue',
          done: false,
        },
        {
          id: 2,
          text: 'vue 进阶',
          done: false,
        },
        {
          id: 3,
          text: '精通 vue',
          done: false,
        },
      ],
    };
  },
  computed: {
    filteredTodos: function () {
      console.log(this.todoList);
      return this.todoList.filter((item) => !item.done);
    },
  },
  methods: {
    handleClick() {
      console.log(`点击按钮：${this.user.name}`);
    },
    toggleTodo(id) {
      const index = this.todoList.findIndex((item) => item.id === id);
      const isDone = this.todoList[index].done;
      this.todoList[index].done = !isDone;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
