<template>
  <div id="app">
    <BaseLayout>
      <template v-slot:[baseName]> This is Header </template>
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
      baseName: 'default',
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
