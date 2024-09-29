<template>
  <div>
    <button @click="handleSubmit">{{ isShow ? "Ẩn" : "Hiện" }}</button>
  </div>
</template>

<script setup>
import { ref } from "vue";

const isShow = ref(false);
const handleSubmit = () => {
  isShow.value = !isShow.value;
};
</script>

<style></style>
