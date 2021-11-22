<template>
  <li>
     {{ todo.text }}
      <a href="#" @click="$emit('removeElement' , todo.key)"><span class="icon"><i class="fa fa-trash"></i></span></a>
      <a href=""><span class="icone"><i class="fas fa-edit"></i></span></a>
  </li>
</template>

<script>
    export default{
      emits: ['removeElement'],
      props:{
          todo :{
          type : Object,
          required : true,
        }
      }
    }
</script>