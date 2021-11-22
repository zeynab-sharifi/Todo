<template>
  <li v-if="editMode == false">
    {{todo.text}}
      <a href="#" @click="$emit('removeElement' , todo.key)"><span class="icon"><i class="fa fa-trash"></i></span></a>
      <a href="#" @click="enabelClick"><span class="icone"><i class="fas fa-edit"></i></span></a>
  </li>
  <li v-if="editMode == true">
    <input type="text" v-model="todoText">
      <a href="#" @click="editTodo"><span class="icone"><i class="fas fa-edit"></i></span></a>
  </li>
</template>

<script>
    export default{
      emits: ['removeElement' , 'edited-todo'],
      props:{
          todo :{
          type : Object,
          required : true,
        }
      },
      data(){
        return {
          editMode : false,
          todoText : 'lhn'
        }
      },
      methods :{
        enabelClick(){
          this.editMode = true;
          this.todoText = this.todo.text;
        },
        editTodo(){
          this.editMode = false;
          this.$emit('edited-todo', { key : this.todo.key , text : this.todoText});
          this.todoText = '';
        }
      }
    }
</script>