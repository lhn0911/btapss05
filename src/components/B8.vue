<template>
  <div>
    <button @click="handleIncrease">Tăng</button>
    <button @click="handleDecrease">Giảm</button>
    <ul>
      <li v-for="number in arrayNumbers" :key="number">{{ number }}</li>
    </ul>
  </div>
</template>

<script setup>
import { ref } from "vue";
const arrayNumbers = ref([1, 4, 2, 3, 5, 8, 7, 6]);
const handleIncrease = () => {
  arrayNumbers.value.sort((a, b) => a - b);
};
const handleDecrease = () => {
  arrayNumbers.value.sort((a, b) => b - a);
};
</script>

<style></style>
