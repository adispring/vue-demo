<template>
  <div id="app">
    <BaseLayout>
      <template v-slot:[baseName]> This is Header </template>
    </BaseLayout>
    <button @click="handleClick">按钮</button>
  </div>
</template>

<script type="text/babel">
import BaseLayout from './components/BaseLayout.vue';

export default {
  name: 'App',
  components: {
    BaseLayout,
  },
  data() {
    return {
      baseName: 'default',
      user: {
        name: 'adi',
      },
    };
  },
  methods: {
    handleClick() {
      console.log(`点击按钮：${this.user.name}`);
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
