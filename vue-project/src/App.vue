<template>
  <h1>Проект на Vue.js</h1>
  <button @click = 'counter++'>Счётчик {{ counter }}</button>
</template>

<script setup>
import {ref} from 'vue'
const counter = ref(0)
const counter2 = 0

</script>