<template>
  <button class="button" :class="modifications">
    <slot />
  </button>
</template>

<script>
export default {
  props: {
    type: String,
  },
  computed: {
    modifications() {
      return {
        'button--danger': !!this.type,
      };
    },
  },
};
</script>

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
  &--danger {
    background: var(--error-color);
    border: 2px solid var(--error-color);

    &:hover {
      color: var(--error-color);
      background: transparent;
    }
  }
}
</style>