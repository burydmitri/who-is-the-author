<template>
  <div class="card">
    <AspectRatio :ratio="16 / 9">
      <img
        class="card__image"
        src="https://d7hftxdivxxvm.cloudfront.net/?height=334&quality=80&resize_to=fill&src=https%3A%2F%2Fartsy-media-uploads.s3.amazonaws.com%2FDX2ifF8rooHgPwQk2ADNdA%252FEmergingMag.png&width=445"
        alt=""
      />
    </AspectRatio>
    <!-- <span class="card__author">Joe Cadoe</span>
    <div class="card__wrapper">
        <button class="card__button">INFO</button>
        <button class="card__button">ADD</button>
    </div>  -->
  </div>
</template>

<script>
import { AspectRatio } from "radix-vue";

export default {
  components: {
    AspectRatio,
  },
};
</script>

<style lang="less" scoped>
.card {
  width: 100%;

  border-radius: 10px;
  overflow: hidden;

  position: relative;
  &:hover {
    opacity: 0.8;
  }

  &__image {
    object-fit: cover;
    width: 100%;
    height: 100%;
  }
}
</style>