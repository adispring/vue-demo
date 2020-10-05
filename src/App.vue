<template>
  <div id="app">
    <BaseLayout>
      <template v-slot:header>
        <h1>This is Header</h1>
      </template>
      This is content
      <template v-slot:footer>
        <h2>This is Footer</h2>
      </template>
    </BaseLayout>
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
