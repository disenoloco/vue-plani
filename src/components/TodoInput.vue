<template>
  <div class="inputBox shadow">
    <input type="text" v-model="newTodoItem" placeholder="Type what you have to do." v-on:keyup.enter="addTodo">
    <span class="addContainer" v-on:click="addTodo">
      <transition name="fade">
        <i class="addBtn xi-plus" aria-hidden="true"></i>
      </transition>
    </span>
  </div>
</template>

<script>
export default {
  data() {
    return {
      newTodoItem: ''
    }
  },
  methods: { 
    addTodo() {
      if(this.newTodoItem !== ""){
        var value = this.newTodoItem && this.newTodoItem.trim();
        localStorage.setItem(this.newTodoItem, this.newTodoItem);  
      }
      this.clearInput();
    },
    clearInput(){
      this.newTodoItem = '';
    }
  }
}
</script>
<style>
  input:focus { outline: none; }
  .inputBox { background: white; max-width: 1000px; height: 50px; line-height: 50px; margin: 0 auto; border-radius: 5px; }
  .inputBox input { border-style: none; font-size: .9rem; }
  .addContainer { float: right; background: linear-gradient(to right, #6478FB, #8763FB); display: block; width: 3rem; height: 100%; border-radius: 0 5px 5px 0; cursor: pointer; }
  .addBtn { color: #fff; vertical-align: middle; font-size: 1.2rem; }
</style>
