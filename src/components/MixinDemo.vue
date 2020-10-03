<script>
import Vue from 'vue';
// 定义一个混入对象
var myMixin = {
  created: function () {
    this.hello();
  },
  methods: {
    hello: function () {
      console.log('hello from mixin!');
    },
  },
};
var Profile = Vue.extend({
  mixins: [myMixin],
  template: '<p>{{firstName}} {{lastName}} aka {{alias}}</p>',
  data: function () {
    return { firstName: 'Walter', lastName: 'White', alias: 'Heisenberg' };
  },
});
export default Profile;
</script>
