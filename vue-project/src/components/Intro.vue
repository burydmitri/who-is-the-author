<template>
  <div class="intro">
    <h1 class="intro__title">WhoWho</h1>
    <p class="intro__subtitle">Try to guess the authors of the artistic works of art!</p>

    <div class="intro__wrapper">
      <Button>Learn new</Button>
      <Button>Repeat</Button>
    </div>
  </div>
</template>

<script>
import Button from './Button.vue'
export default {
  components: { Button }
}
</script>

<style lang="less" scoped>
.intro {
  text-align: center;

  &__title {
    font-size: 64px;
    line-height: 72px;
  }
  &__subtitle {
    margin-bottom: 25px;
  }

  &__wrapper {
    gap: 20px;
    display: flex;
    justify-content: center;
  }
}
</style>