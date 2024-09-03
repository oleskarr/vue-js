<template>
  <main>
    <div class="container">
      <img src="../assets/img/cabbage.png" />
      <p>
        Капуста давно и прочно вошла в рацион нашего питания и принадлежит к
        числу важнейших овощных растений. Она также является неотъемлемой частью
        таких традиционных блюд, как: борщ, щи, солянка, тушеная капуста,
        голубцы, капустная запеканка и конечно квашеная капуста.
      </p>
      <p style="width: 907px;">
        Капуста не только популярный, но и полезный продукт: она богата
        витаминами А, В1, Р, К, В6, U. Капуста является лидером среди овощей по
        содержанию витамина С, причем он сохраняется в капусте как при
        длительном хранении в сыром виде, так и при термической обработке. В ней
        также много минералов - сера, кальций, калий и фосфор, клетчатки и воды.
      </p>
    </div>
    <div class="likes">
      <!-- Картинка по умолчанию -->
      <img src="../assets/img/stayble.png" class="f" />

      <!-- Картинка при наведении -->
      <img src="../assets/img/cursor-on.png" class="s" />

      <!-- Картинка при клике -->
      <img
        src="../assets/img/liked.png"
        class="th"
        @click="toBlock"
        :class="{ display:isClicked }"
      />
    </div>
  </main>
</template>

<style>
main{
  position: relative;
}
.container {
  display: flex;
  gap: 10px;
  flex-wrap: wrap;
  padding: 30px;
  align-items: center;
}

.container p {
  width: 461px;
  height: 259px;
  font-size: 24px;
  color: #b54b62;
}

.likes {
  display: flex;
  gap: 0;
  width: max-content;
}

.likes .s {
  display: none;
}

.likes .th {
  display: none; 
}
.likes:hover .f {
  display: none;
}

.likes:hover .s {
  display: block;
}
</style>


<script setup>
import { ref } from 'vue'

const isClicked = ref('none');


const toBlock = () => {
  isClicked.value = isClicked.value === 'none' ? 'block' : 'none';
};
</script>