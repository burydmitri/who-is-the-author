<template>
  <main class="main">
    <h1 class="main__title">Hello, World!</h1>
  </main>
</template>

<script >
</script>

<style lang="less" scoped>
  .main {
    height: 100vh;
    width: 100%;

    display: flex;
    align-items: center;
    justify-content: center;
  
    &__title {
      font-size: 52px;

      color: var(--primary-color)
    }
  }

</style>
