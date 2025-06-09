<script setup lang="ts">

import { computed,ref } from 'vue';
const originalPrice = ref(100);
const discount = ref();
const finalPrice = computed(() => {
  return originalPrice.value - discount.value ;
});


</script>

<template>
  <div class="price-block">
    <input type="number" v-model="discount" placeholder="Original Price" />
    <p> Original Price: {{ originalPrice }}</p>
    <p> Discount: {{ discount }}</p>
    <p> Final Price: {{ finalPrice }}</p>
  </div>
</template>

<style scoped>

</style>
