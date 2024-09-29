<template>
  <div>
    <button @click="handleActive">hiện</button>
    <button @click="handleUnActive">ẩn</button>
    <p v-show="isVisible === true">Thông báo :Welcome to Rikkei Education</p>
    <p v-show="isVisible === false"></p>
  </div>
</template>

<script setup>
import { ref } from "vue";
const isVisible = ref(false);
const handleActive = () => {
  isVisible.value = true;
};
const handleUnActive = () => {
  isVisible.value = false;
};
</script>

<style></style>
