<template>
  <div>
    <p v-if="role === admin">quyền hạn của bạn là:admin</p>
    <p v-else-if="role === user">quyền hạn của bạn là:user</p>
    <p v-else-if="role === guest">quyền hạn của bạn là:guest</p>
    <p v-else></p>
  </div>
</template>

<script>
const role = "admin";
</script>

<style></style>
