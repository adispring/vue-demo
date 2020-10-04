<template>
  <span>
    <slot v-bind:user1="user">{{ user.lastName }}</slot>
  </span>
</template>

<script>
export default {
  data: () => {
    return {
      user: {
        lastName: 'zengdi',
        firstName: 'wang',
      },
    };
  },
};
</script>

<style></style>
