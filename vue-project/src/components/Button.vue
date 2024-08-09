<template>
  <button class="button">
    <slot />
  </button>
</template>

<style lang="less" scoped>
.button {
  width: 40%;
  font-weight: 700;
  color: var(--background-color);
  background: var(--primary-color);

  padding: 10px;
  border: 2px solid var(--primary-color);
  border-radius: 10px;

  &:hover {
    color: var(--text-color);
    background: transparent;
  }
  &:active {
    transform: scale(1.1);
  }
}
</style>