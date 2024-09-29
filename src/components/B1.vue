<template>
  <div>
    <p v-show="isShow">Rekkeiacademy</p>
    <button @click="handleSubmit">Hiện</button>
  </div>
</template>

<script setup>
import { ref } from "vue";

const isShow = ref(false);
const handleSubmit = () => {
  isShow.value = true;
};
</script>

<style></style>
