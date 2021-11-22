<template>
    <ul class="todoList">
          <todo v-for="(item , index) in todos" :todo="item" :key="index" @removeElement="$emit('removeElement' , $event)"></todo>
    </ul>
</template>
<script>
import Todo from './Todo.vue'
    

export default{
    props : {
      todos : {
          type : Array,
          required : true,
      }
  },
  components :{
    Todo 
  },
  
}
</script>