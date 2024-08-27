<template>
  <h1>Проект на Vue.js</h1>
  <input type="checkbox" id="checkbox" v-model="checked" />
  <label for="checkbox">{{ checked }}</label>
</template>

<script setup>
import {ref} from 'vue'
const counter = ref(0)
const checked = ref('true') 
</script>