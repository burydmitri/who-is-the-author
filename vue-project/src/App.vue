<template>
  <main class="app">
    <Intro />
  </main>
</template>

<script>
import Intro from './components/Intro.vue'
export default {
  components: { Intro }
}
</script>

<style lang="less" scoped>
.app {
  min-height: 100vh;
  height: 100%;
  width: 100vw;

  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
</style>
