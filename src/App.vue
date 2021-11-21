<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
      <div class="wrapper">
        <header>Todo App</header>
        <div class="inputField">
          <input type="text" placeholder="Add your new todo">
          <button><i class="fas fa-plus"></i></button>
        </div>
        <ul class="todoList">
          <li>
            joscos
            <span class="icon"><i class="fa fa-trash"></i></span>
            <span class="icone"><i class="fas fa-edit"></i></span>
          </li>
          <li>
            sdjpsdj
            <span class="icon"><i class="fa fa-trash"></i></span>
            <span class="icone"><i class="fas fa-edit"></i></span>
          </li>
          <li>
            sdodsvopmals]-pwlcg.uoglufhb.jhhiuoiuiknkbjvs
            <span class="icon"><i class="fa fa-trash"></i></span>
            <span class="icone"><i class="fas fa-edit"></i></span>
          </li>
        </ul>
        <div class="footer">
          <span>You have <span class="pendingTasks"></span> pending tasks</span>
          <button>Clear All</button>
        </div>
      </div>
</template>

<style>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Poppins', sans-serif;
}
::selection{
  color: #ffff;
  background: rgb(142, 73, 232);
}
body{
  width: 100%;
  height: 100vh;
  /* overflow: hidden; */
  padding: 10px;
  background: linear-gradient(to bottom, #26f0c1 0%, #e84949 100%);
}
.wrapper{
  background: #fff;
  max-width: 400px;
  width: 100%;
  margin: 120px auto;
  padding: 25px;
  border-radius: 5px;
  box-shadow: 0px 10px 15px rgba(0,0,0,0.1);
}
.wrapper header{
  font-size: 30px;
  font-weight: 600;
}
.wrapper .inputField{
  margin: 1.5rem 0 3.5rem;
  width: 100%;
  display: flex;
  height: 45px;
}
.inputField input{
  width: 85%;
  height: 100%;
  outline: none;
  border-radius: 3px;
  border: 1px solid #ccc;
  font-size: 17px;
  padding-left: 15px;
  transition: all 0.3s ease;
}
.inputField input:focus{
  border-color: #c0392b;
}
.inputField button{
  width: 50px;
  height: 100%;
  border: none;
  color: #fff;
  margin-left: 5px;
  font-size: 21px;
  outline: none;
  background-color:#e74c3c;
  box-shadow: 0 1px 2px rgba(0, 0, 0, .12);
  cursor: pointer;
  border-radius: 3px;
  transition: all 0.3s ease;
}
.inputField button:hover,
.footer button:hover{
  background-color: #c0392b;
  box-shadow: 0 2px 4px rgba(0, 0, 0, .15);
}
.inputField button.active{
  opacity: 1;
  pointer-events: auto;
}
.wrapper .todoList{
  max-height: 250px;
  overflow-y: auto;
}
.todoList li{
  text-align: left;
  position: relative;
  list-style: none;
  padding: 10px 45px;
  line-height: 45px;
  margin-bottom: 8px;
  background: #f2f2f2;
  border-radius: 3px;
  padding: 0 15px;
  cursor: default;
  overflow: hidden;
}
.todoList li .icon{
  position: absolute;
  background: transparent;
  width: 35px;
  right: 0;
  text-align: center;
  color: #888;
  border-radius: 0 3px 3px 0;
  cursor: pointer;
  transition: all 0.2s ease;
}
.todoList li .icone{
  position: absolute;
  background: transparent;
  width: 35px;
  right: 40px;
  text-align: center;
  color: #888;
  border-radius: 0 3px 3px 0;
  cursor: pointer;
  transition: all 0.2s ease;
}
.todoList li .icon:hover{
  color: #e74c3c;
}
.todoList li .icone:hover{
  color: #68EACC;
}
.wrapper .footer{
  display: flex;
  width: 100%;
  margin-top: 20px;
  align-items: center;
  justify-content: space-between;
}
.footer button{
  padding: 6px 10px;
  border-radius: 3px;
  border: none;
  outline: none;
  color: #fff;
  font-weight: 400;
  font-size: 16px;
  margin-left: 5px;
  background: #e74c3c;
  cursor: pointer;
  user-select: none;
  transition: all 0.3s ease;
}
.footer button.active{
  opacity: 1;
  pointer-events: auto;
}
</style>
