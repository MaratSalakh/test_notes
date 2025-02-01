<script setup lang="ts">
import ButtonUI from "./components/ButtonUI.vue";
import NoteUI from "./components/NoteUI.vue";
</script>

<template>
  <ButtonUI icon="next" variant="basic">Вход</ButtonUI>

  <ButtonUI icon="close" variant="rounded"></ButtonUI>

  <NoteUI header="Header">Note for everybody</NoteUI>
</template>

<style scoped></style>
