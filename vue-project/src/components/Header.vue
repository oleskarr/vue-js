<template>
     <header >
    <h1>Полезные свойства капусты</h1>
    <nav ref="menu" class="menu">
      <ul>
        <li  @click="toggleMenu"><img src="../assets/img/apps 1.png" ></li>
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
<script>
import { ref } from 'vue';

export default {
  setup() {
    const isMenuVisible = ref(false); // Состояние видимости меню
    const menu = ref(null); // Ссылка на элемент DOM

    const toggleMenu = () => {
      if (isMenuVisible.value) {
        // Если меню видно, скрываем его
        menu.value.style.transition = 'right 0.5s ease, transform 0.5s ease'; // Плавный переход
        menu.value.style.right = '-300px'; // Скрываем меню
        menu.value.style.transform = 'translateX(0)'; // Возвращаем исходное положение
      } else {
        // Если меню скрыто, показываем его
        menu.value.style.transition = 'right 0.5s ease, transform 0.5s ease'; // Плавный переход
        menu.value.style.right = '50%'; // Перемещаем меню в центр
        menu.value.style.transform = 'translateX(50%)'; // Центрируем по оси X
      }
      isMenuVisible.value = !isMenuVisible.value; // Переключаем состояние меню
    };

    return {
      menu,
      toggleMenu
    };
  }
};
</script>