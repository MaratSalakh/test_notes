<script setup lang="ts">
import ButtonUI from "./components/ButtonUI.vue";
import NoteUI from "./components/NoteUI.vue";
import MenuUI from "./components/MenuUI.vue";
</script>

<template>
  <div class="mainBlock">
    <MenuUI></MenuUI>
    <div class="workArea">
      <div class="contentBlock">
        <h1>Мои заметки</h1>
        <h3>Не забывай о важном, храни его в облаке</h3>
      </div>
      <div>
        <img
          width="627"
          height="604"
          src="./assets/mainPicture.png"
          alt="notes img"
        />
      </div>
    </div>
  </div>
</template>

<style scoped>
.mainBlock {
  max-height: 100vh;
  max-width: 100vw;
}
.contentBlock {
  display: flex;
  flex-direction: column;
  justify-content: start;
  align-items: start;
  row-gap: 40px;
}
.workArea {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-inline: 80px;
}
</style>
