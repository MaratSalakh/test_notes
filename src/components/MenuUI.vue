<script setup lang="ts">
import logo from "../assets/logo.png";
import ButtonUI from "./ButtonUI.vue";
</script>

<template>
  <div class="menu">
    <img width="218" height="50" :src="logo" alt="" />
    <div class="profile">
      <ButtonUI icon="next" variant="basic">Вход</ButtonUI>
    </div>
  </div>
</template>

<style scoped>
.menu {
  height: 96px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-inline: 80px;
}
.profile {
  display: flex;
  justify-content: center;
  align-items: center;
  column-gap: 12px;
}
</style>
