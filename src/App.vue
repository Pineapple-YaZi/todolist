<template>
  <div class="todoapp">
    <TodoHeader @addTask="onAdd"></TodoHeader>
    <TodoMain :arr="list" @delTask="onDel"></TodoMain>
    <TodoFooter :arr="list"></TodoFooter>
  </div>
</template>

<script>
// 导入组件
import TodoHeader from "./components/TodoHeader.vue";
import TodoMain from "./components/TodoMain.vue";
import TodoFooter from "./components/TodoFooter.vue";
// 导入样式
import "./styles/base.css";
import "./styles/index.css";

export default {
  data() {
    return {
      list: [
        { id: 100, name: "吃饭", isDone: true },
        { id: 201, name: "睡觉", isDone: false },
        { id: 103, name: "打豆豆", isDone: true },
      ],
    };
  },
  // 定义标签
  components: {
    TodoHeader,
    TodoMain,
    TodoFooter,
  },

  created() {},
  computed: {},

  methods: {
    onAdd(task) {
      return this.list.push({
        id: this.list[this.list.length - 1]
          ? this.list[this.list.length - 1].id + 1
          : 100,
        name: task,
        isDone: false,
      });
    },
    onDel(id) {
      const index = this.list.findIndex(item =>item.id===id)
      this.list.splice(index,1)
    },
  },
};
</script>

<style scoped>
</style>
