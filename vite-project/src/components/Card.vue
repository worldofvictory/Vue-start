<script setup lang="ts">
 
 import {ref} from 'vue';
 
 const text = ref("")
const props = defineProps<{
arrayCard: {
  name: string;
  age: number;
  alt: string;
  src: string;
}[];
}>();




</script>

<template>
    
 <ul v-for="card in arrayCard" :key="card.name" class="cards">
    <li> 
        <img :src="card.src" :alt="card.alt"  style="width: 50px;"/>
        {{ card.name }} {{ card.age }}</li>
 </ul>
 
</template>

<style scoped>
ul {
    list-style: none;
}
</style>
