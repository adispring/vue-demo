<template>
  <div>
    <slot v-bind:student="student">{{ student.name }}</slot>
    <slot name="teacher" v-bind:t="teacher">{{ teacher.name }}</slot>
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
      teacher: {
        name: 'wang',
        id: 12315,
      },
    };
  },
};
</script>

<style></style>
