<template>
  <main class="app">
    <Intro class="app__intro"/>
    <Cards class="app__cards"/>
    <Repeat />
  </main>
</template>

<script>
import Intro from './components/Intro.vue'
import Cards from './components/Cards.vue'
import Repeat from './components/Repeat.vue'

export default {
  components: { Intro, Cards, Repeat }
}
</script>

<style lang="less" scoped>
.app {
  width: 100%;
  max-width: 1080px;
  min-height: 100vh;

  display: flex;
  flex-direction: column;
  align-items: center;

  margin: 0 auto;
  padding: 300px 20px 20px;

  &__intro, &__cards {
    margin-bottom: 50px;
  }

}
</style>
