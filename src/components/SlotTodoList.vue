<template>
  <ul>
    <li
      v-for="todo in filteredTodos"
      v-bind:key="todo.id"
      @click="toggle(todo.id)"
    >
      <slot name="todo" v-bind:todo="todo">{{ todo.text }}</slot>
    </li>
  </ul>
</template>

<script>
export default {
  props: ['filteredTodos', 'toggle'],
};
</script>

<style></style>
