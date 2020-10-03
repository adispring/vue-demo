<template>
  <div id="app">
    <TodoList />
    <NavigationLink url="https://www.google.com">Your Profile</NavigationLink>
    <MixinDemo></MixinDemo>
  </div>
</template>

<script type="text/babel">
import TodoList from './components/TodoList.vue';
import NavigationLink from './components/NavigationLink.vue';
import MixinDemo from './components/MixinDemo.vue';

export default {
  name: 'App',
  components: {
    TodoList,
    NavigationLink,
    MixinDemo,
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
