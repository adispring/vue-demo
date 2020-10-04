<template>
  <div id="app">
    <TodoList />
    <NavigationLink url="https://www.google.com"
      >Your Profile: {{ user.name }}</NavigationLink
    >
    <MixinDemo></MixinDemo>
    <SlotDemo>
      <template v-slot:header>
        <h1>这是 header！</h1>
      </template>
      <template>这是 default slot</template>
      <template v-slot:footer>这是页脚</template>
    </SlotDemo>
    <SubmitButton>Save</SubmitButton>
    <CurrentUser>
      <template v-slot:default="a">
        {{ a.user1.firstName }}
      </template>
    </CurrentUser>
  </div>
</template>

<script type="text/babel">
import TodoList from './components/TodoList.vue';
import NavigationLink from './components/NavigationLink.vue';
import MixinDemo from './components/MixinDemo.vue';
import SlotDemo from './components/SlotDemo.vue';
import SubmitButton from './components/submit-button.vue';
import CurrentUser from './components/CurrentUser.vue';

export default {
  name: 'App',
  components: {
    TodoList,
    NavigationLink,
    MixinDemo,
    SlotDemo,
    SubmitButton,
    CurrentUser,
  },
  data: () => ({
    user: {
      name: 'adi',
    },
    slotProps: {
      user: {
        firstName: '第一名称',
      },
    },
  }),
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
