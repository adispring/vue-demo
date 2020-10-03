<template>
  <a v-bind:href="url" class="nav-link">
    <slot></slot>
  </a>
</template>

<script>
export default {
  name: 'NavigationLink',
  props: ['url'],
};
</script>

<style scoped>
.nav {
  &-link {
  }
}
.nav-link {
  color: red;
}
</style>
