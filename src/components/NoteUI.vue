<script setup lang="ts">
import ButtonUI from "./ButtonUI.vue";
defineProps<{ header: string }>();
</script>

<template>
  <div class="note">
    <div class="note_header">
      <h4 class="header">{{ header }}</h4>
    </div>
    <div class="note_body">
      <div class="text_normal"><slot></slot></div>
    </div>
    <div class="note_footer">
      <ButtonUI icon="close" variant="basic">Удалить</ButtonUI>
    </div>
  </div>
</template>

<style scoped>
.note {
  display: flex;
  flex-direction: column;
  width: 30%;
}

.note_header {
  padding: 20px 28px;
  background: linear-gradient(-135deg, transparent 23px, #b1c909 0);
  border-radius: 12px 12px 0 0;
  border-bottom: 1px solid #a5bb0c;
}

.header {
  margin: 0;
}

.note_body {
  padding: 20px 28px 28px 28px;
  background-color: #b1c909;
}

.note_footer {
  background-color: #b1c909;
  border-radius: 0 0 12px 12px;
  display: flex;
  justify-content: end;
  padding: 8px 8px;
}
</style>
