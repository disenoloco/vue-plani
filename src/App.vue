<template>
  <div id="app">
    <TodoHeader></TodoHeader>
    <TodoInput></TodoInput>
    <!-- 
    <TodoList></TodoList>
    <TodoFooter></TodoFooter> 
    -->
  </div>
</template>

<script>
  import TodoHeader from './components/TodoHeader.vue'
  import TodoInput from './components/TodoInput.vue'
  import TodoList from './components/TodoList.vue'
  import TodoFooter from './components/TodoFooter.vue'

  export default {
    components: {
      'TodoHeader': TodoHeader,
      'TodoInput': TodoInput,
      'TodoList': TodoList,
      'TodoFooter': TodoFooter
   }
  }
</script>
<style>
  #app { font-family: 'Open Sans', sans-serif; }
  body { text-align: center; background-color: #f6f6f6; }
  input { border-style: groove; width: 90%; }
  button { border-style: groove; }
  .shadow { box-shadow: 1px 5px 10px rgba(0, 0, 0, 0.08); }
</style>
