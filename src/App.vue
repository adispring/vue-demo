<template>
  <div id="app">
    <DynamicParam></DynamicParam>
  </div>
</template>

<script type="text/babel">
import DynamicParam from './components/DynamicParam.vue';

export default {
  name: 'App',
  components: {
    DynamicParam,
  },
  data() {
    return {
      user: {
        name: 'adi',
      },
    };
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
