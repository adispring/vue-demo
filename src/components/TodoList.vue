<template>
  <div class="ToDoList">
    <h1 v-html="title">My TodoList</h1>
    <div>
      <input name="" type="text" value="" v-model="newItem" />
      <button @click="addNewItem">添加</button>
    </div>
    <ul>
      <li v-for="item in items" :key="item.id">
        <!-- 代办事项 -->
        <span v-text="item.title"></span>
        <button v-on:click="toggleFinish(item)">完成</button>
      </li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: 'ToDoList',
    data() {
      return {
        id: 0,
        newItem: '',
        title: '<span></span> this is a todo list',
        items: [],
      };
    },
    methods: {
      toggleFinish(recycleItem) {
        console.log(recycleItem.id);
        this.items.forEach((item, index) => {
          if (item.id === recycleItem.id) {
            this.items.splice(index, 1);
          }
        });
        console.log(this.items);
      },
      addNewItem() {
        this.items.push({
          id: this.id,
          title: this.newItem,
        });
        this.id++;
        this.newItem = '';
      },
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
    margin-top: 10px;
  }
  a {
    color: #42b983;
  }
</style>
