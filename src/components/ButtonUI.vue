<script setup lang="ts">
import entryIcon from "./../assets/next.svg";
import closeIcon from "./../assets/close.svg";
import userIcon from "./../assets/user.svg";
import plusIcon from "./../assets/user.svg";
defineProps<{ variant: string; disabled?: boolean; icon: string }>();

const buttonClass = (disabled: boolean | undefined) => {
  if (disabled) {
    return "disabledButton ";
  }

  return "activeButton";
};
</script>

<template>
  <button
    v-if="variant === 'basic'"
    :class="[buttonClass(disabled), 'basicButton']"
  >
    <img
      v-if="icon === 'next'"
      height="32"
      width="32"
      :src="entryIcon"
      alt="entry button"
    />
    <img
      v-else-if="icon === 'close'"
      height="16"
      width="16"
      :src="closeIcon"
      alt="close button"
    /><slot></slot>
  </button>
  <button v-else :class="[buttonClass(disabled), 'roundedButton']">
    <img
      v-if="icon === 'next'"
      height="32"
      width="32"
      :src="entryIcon"
      alt="entry button"
    />
    <img
      v-else-if="icon === 'close'"
      height="16"
      width="16"
      :src="closeIcon"
      alt="close button"
    />
    <img
      v-else-if="icon === 'user'"
      width="20"
      height="28"
      :src="userIcon"
      alt="close button"
    />
    <img
      v-else-if="icon === 'plus'"
      width="16"
      height="16"
      :src="plusIcon"
      alt="close button"
    />
  </button>
</template>

<style scoped>
.activeButton {
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
  min-height: 56px;
  padding: 0px 24px;
  column-gap: 12px;
}

.roundedButton {
  min-width: 56px;
  min-height: 56px;
}

:hover.activeButton {
  background-color: #97ab0d;
}

:active.activeButton {
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
