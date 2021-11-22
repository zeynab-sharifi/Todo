<template>
    <div class="inputField">
          <input type="text" v-model="todoText" placeholder="Add your new todo">
          <button v-on:click="submit"><i class="fas fa-plus"></i></button>
        </div>
</template>
<script>
  export default{
    emits : ['add-todo'],
    data(){
      return{
        todoText : ''
      }
    },
    methods : {
      submit(){
        this.$emit('add-todo' , this.todoText);
        this.todoText = '';
      }
    }
  }
</script>