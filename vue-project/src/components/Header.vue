<template>
     <header >
    <h1>Полезные свойства капусты</h1>
    <nav>
      <ul>
        <li @click="activeMenu"><img src="../assets/img/apps 1.png" ></li>
        <li><a href="#">Главная</a></li>
        <li><a href="#">Блог</a></li>
        <li><a href="#">О нас</a></li>
        <li><a href="#">Контакты</a></li>
      </ul>
    </nav>
  </header>
</template>

<style>
header{
  position: relative;
  width: fit-content;
  margin: 0;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  overflow-x: hidden;
  background-color: #FECFB0;
}
header h1{
  color: #B54B62;
}
nav{
  position: absolute;
  right: -300px;
 
  display: flex;
  background-color: #B54B62;
  width: fit-content;
  padding: 7px;
  padding-left: 30px;
  padding-right: 30px;
  border-radius: 40px;
  
  ul{
    display: flex;
    list-style: none;
    align-items: center;
    justify-content: center;
    gap: 25px;
    margin: 0;
    padding: 0;
   
    a{
      text-decoration: none;
      color: #E5847B;
      font-size: 15px;
    
    }
  }
}
nav a:hover{
        color: #FECFB0;
      } 
</style>
<script setup>
import {reactive} from 'vue'
const activeMenu = function(){
  
}
</script>