<template>
    <main>
<div class="container">
  <img src="../assets\img\cabbage.png">
  <p>Капуста давно и прочно вошла в рацион
нашего питания и принадлежит к числу
важнейших овощных растений. Она
также является неотъемлемой частью
таких традиционных блюд, как: борщ,
щи, солянка, тушеная капуста, голубцы,
капустная запеканка и конечно
квашеная капуста.</p>
<p style="width: 907px;">Капуста не только популярный, но и полезный продукт: она богата
витаминами А, В1, Р, К, В6, U. Капуста является лидером среди овощей по
содержанию витамина С, причем он сохраняется в капусте как при длительном
хранении в сыром виде, так и при термической обработке. В ней также много
минералов - сера, кальций, калий и фосфор, клетчатки и воды.</p>
</div>
<div class="likes">
  <img src="..\assets\img\stayble.png" class="f">
  <img src="..\assets\img\cursor-on.png" class="s">
  <img src="..\assets\img\liked.png" class="th" @click="toBlock">
</div>

</main>
</template>
<style>
.container{
  display: flex;
  gap: 10px;
  flex-wrap: wrap;
  padding: 30px;
  align-items: center;
  p{
    width: 461px;
    height: 259px;
    font-size: 24px;
    color: #B54B62;
  }
}
.likes{
    display: flex;
    gap: 0;
    width: max-content;
}
.likes .s{
    display: none;
}
.likes .th{
    display: none;
}
.likes:hover .f{
   display: none;
}
.likes:hover .s{
   display: block;
}

</style>
<script setup>
import {ref, reactive } from 'vue';
const toBlock = function(){
 block.blocked=ref('true')
}
const block = reactive({
    blocked :'display:block'
})
</script>