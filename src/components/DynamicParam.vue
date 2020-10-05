<template>
  <a v-bind:[attributeName]="url">点击</a>
</template>

<script>
export default {
  data() {
    return { attributeName: 'href', url: 'https://www.baidu.com' };
  },
};
</script>

<style></style>
