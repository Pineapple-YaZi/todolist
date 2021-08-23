<template>
  <div class="todoapp">
    <TodoHeader></TodoHeader>
    <TodoMain></TodoMain>
    <TodoFooter></TodoFooter>
  </div>
</template>

<script>
// 导入组件
import TodoHeader from "./components/TodoHeader.vue";
import TodoMain from "./components/TodoMain.vue";
import TodoFooter from "./components/TodoFooter.vue";
// 导入样式
import './styles/base.css';
import './styles/index.css'

export default {
  data() {
    return {};
  },
  // 定义标签
  components: {
    TodoHeader,
    TodoMain,
    TodoFooter,
  },

  created() {},

  methods: {},
};
</script>

<style scoped>
</style>
