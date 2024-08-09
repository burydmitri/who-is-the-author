<template>
  <div class="intro">
    <h1 class="intro__title">WhoWho</h1>
    <p class="intro__subtitle">Try to guess the authors of the artistic works of art!</p>

    <div class="intro__wrapper">
      <button class="intro__button">Learn new</button>
      <button class="intro__button">Repeat</button>
    </div>
  </div>
</template>

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

  &__button {
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
}
</style>