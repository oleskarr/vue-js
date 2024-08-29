<template>
   <Header />
   <div class="box">
    <Main />

   <Footer/>
   </div>


</template>

<style>
.box{
  background-color: #FEA896;
border-top-left-radius:60px ;
border-top-right-radius:60px ;

}

</style>

<script setup>
  import Header from './components/Header.vue'
  import Footer from './components/Footer.vue'
  import Main from './components/Main.vue'
</script>

