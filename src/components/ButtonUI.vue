<script setup lang="ts">
import entryIcon from "./../assets/next.svg";
import closeIcon from "./../assets/close.svg";
defineProps<{ variant: string; disabled?: boolean }>();

const buttonClass = (disabled: boolean | undefined) => {
  if (disabled) {
    return "disabledButton ";
  }

  return "button";
};
</script>

<template>
  <button
    v-if="variant === 'basic'"
    :class="[buttonClass(disabled), 'basicButton']"
  >
    <img
      height="32"
      width="32"
      :src="entryIcon"
      alt="entry button"
    /><slot></slot>
  </button>
  <button v-else :class="[buttonClass(disabled), 'closeButton']">
    <img height="16" width="16" :src="closeIcon" alt="close button" />
  </button>
</template>

<style scoped>
.button {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #b1c909;
  color: white;
  border-radius: 32px;
  border-style: none;
  cursor: pointer;
  font-size: 20px;
}

.basicButton {
  padding: 12px 24px;
  column-gap: 12px;
}

.closeButton {
  padding: 20px;
}

:hover.button {
  background-color: #97ab0d;
}

:active.button {
  background-color: #819400;
}

.disabledButton {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #9da5af;
  color: white;
  border-radius: 32px;
  border-style: none;
  cursor: pointer;
  font-size: 20px;
}
</style>
