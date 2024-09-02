<template>
  <footer :style="{ height: footerHeight }" @click="toggleHeight">
   
    <div class="share">
      <img src="../assets/img/vkontacte.png" />
      <img src="../assets/img/odnoklassniki 1.png" />
      <img src="../assets/img/telegram.png" />
    </div>
    <p>Поделиться</p>
  </footer>
</template>

<style scoped>
footer p {
  font-size: 24px;
  color: #fecfb0;
  margin-top: 5px;
  border-top-left-radius: 10px;
  border-top-right-radius: 10px;

}

footer img {
  width: 32px;
  height: 32px;
}

footer {
  position: absolute;
  margin-top: -40px;
  background-color: #b54b62;
  width: max-content;
  border-top-left-radius: 10px;
  border-top-right-radius: 10px;
  display: flex;
  flex-direction: column;
  align-items: center;
  overflow-y: hidden;
  margin-left: 50px;
  height: 40px;
  transition: height 0.3s ease; 
 
}
.share {
  display: flex;
  gap: 25px;
  padding: 14px;
}
</style>

<script setup>
import { ref } from 'vue';

const footerHeight = ref('40px'); // Начальная высота

const toggleHeight = () => {
  footerHeight.value = footerHeight.value === '40px' ? 'max-content' : '40px';
};
</script>
