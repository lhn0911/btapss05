<template>
  <div>
    <button @click="handleIncrease">Tăng</button>
    <button @click="handleDecrease">Giảm</button>
    <ul>
      <li v-for="number in filteredNumbers" :key="number">{{ number }}</li>
    </ul>
  </div>
</template>

<script setup>
import { ref, computed } from "vue";
const arrayNumbers = ref([1, 4, 2, 3, 5, 8, 7, 6]);
const sortOrder = ref("increase");
const filteredNumbers = computed(() => {
  const evenNumbers = arrayNumbers.value.filter((number) => number % 2 === 0);
  return sortOrder.value === "increase"
    ? evenNumbers.sort((a, b) => a - b)
    : evenNumbers.sort((a, b) => b - a);
});
const handleIncrease = () => {
  sortOrder.value = "increase";
};
const handleDecrease = () => {
  sortOrder.value = "decrease";
};
</script>

<style></style>
