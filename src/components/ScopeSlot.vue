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
        name: 'wangzengdi',
        id: 12306,
        gender: 'male',
      },
      teacher: {
        name: 'Yuri',
        id: 12315,
        gender: 'female',
      },
    };
  },
};
</script>

<style></style>
