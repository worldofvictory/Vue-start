<script setup lang="ts">
 
 import {ref} from 'vue';
 import Cards from './components/Cards.vue';
 const text = ref("")

</script>

<template>
  <!--Esercizio 1-->
  <!--<div class="container">
    <button @click="flag =!flag"> Click!</button>
    <h2 class="title-esercizio1" v-if = "flag">Hello</h2>
    <h2  v-else> Bye Bye</h2>
  </div>-->

  <Cards />

  <!--Esercizio 2-->
  <!--
   <div class="container-2">
    <input type="text" class="input" v-model="text">
    <p>{{ text }} </p>
   </div>-->
    
</template>

<style scoped>

</style>
