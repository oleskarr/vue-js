<template>
  <footer  @click="toggleHeight">
   
    <div class="share" :style="{ display: isitBlock }" >
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
  margin-bottom: 5px;
  border-top-left-radius: 10px;
  border-top-right-radius: 10px;

}

footer img {
  width: 32px;
  height: 32px;
}

footer {
  position: relative;
  margin-top: -40px;
  background-color: #b54b62;
  width: 174px;
  border-top-left-radius: 10px;
  border-top-right-radius: 10px;
  display: flex;
  flex-direction: column;
  align-items: center;
  
  margin-left: 50px;
  
  
}
.share {
  background-color: #b54b62;
  border-top-left-radius: 10px;
  border-top-right-radius: 10px;
  bottom: 30px;
  position: absolute;
  display: none;
  gap: 25px;
  padding: 14px;
}
</style>

<script setup>
import { ref } from 'vue';

const isitBlock = ref('none'); // Начальная высота

const toggleHeight = () => {
  isitBlock.value = isitBlock.value === 'none' ? 'flex' : 'none';
};
</script>
