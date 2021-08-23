<template>
  <footer class="footer">
    <span class="todo-count"
      >剩余：<strong>{{ count }}</strong></span
    >
    <ul class="filters">
      <li>
        <a class="selected" href="javascript:;">全部</a>
      </li>
      <li>
        <a href="javascript:;">未完成</a>
      </li>
      <li>
        <a href="javascript:;">已完成</a>
      </li>
    </ul>
    <button class="clear-completed">清除已完成</button>
  </footer>
</template>

<script>
export default {
  props: ["arr"],
  data() {
    return {};
  },
  computed: {
    // 计算未完成的数组项
    count: {
      set() {
        this.arr.filter((item) => !item.isDone).length;
      },
      get() {
        return this.arr.filter((item) => !item.isDone).length;
      },
    },
  },
};
</script>