<template>
  <div>
    <slot v-bind:student="student">{{ student.name }}</slot>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      student: {
        name: 'zengdi',
        id: 12306,
      },
    };
  },
};
</script>

<style></style>
