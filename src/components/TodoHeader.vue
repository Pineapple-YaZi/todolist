<template>
  <header class="header">
    <h1>todos</h1>
    <input id="toggle-all" class="toggle-all" type="checkbox" >
    <label for="toggle-all"></label>
    <input
      class="new-todo"
      placeholder="输入任务名称-回车确认"
      autofocus
      @keyup.enter="onAdd"
      v-model.trim="task"
    />
  </header>
</template>

<script>
export default {
 methods:{
   onAdd(){
     if(this.task==='') return alert('请输入您要执行的任务名~')
     this.$emit('addTask', this.task)
     this.task = ''
   }
 },
 data(){
   return {
     task:''
   }
 }
}
</script>