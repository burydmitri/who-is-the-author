<template>
  <div class="repeat">
    <div class="repeat__wrapper flip-left">
      <div class="card repeat__card">
        <img
          class="repeat__image"
          src="https://d7hftxdivxxvm.cloudfront.net/?height=334&quality=80&resize_to=fill&src=https%3A%2F%2Fartsy-media-uploads.s3.amazonaws.com%2FDX2ifF8rooHgPwQk2ADNdA%252FEmergingMag.png&width=445"
          alt="author"
        />
        <div class="back">
          <h2 class="card__author">Joe Cadoe</h2>
          <p class="card__name">"Spirit of nature"</p>
        </div>
      </div>
    </div>
    <!-- <img
      class="repeat__image"
      src="https://d7hftxdivxxvm.cloudfront.net/?height=334&quality=80&resize_to=fill&src=https%3A%2F%2Fartsy-media-uploads.s3.amazonaws.com%2FDX2ifF8rooHgPwQk2ADNdA%252FEmergingMag.png&width=445"
      alt="author"
    />
    <h2 class="popover__author">Joe Cadoe</h2>
    <p class="popover__name">"Spirit of nature"</p> -->
    <div class="repeat__buttons-wrapper">
      <Button class="repeat__button" type="danger">Delete</Button>
      <Button class="repeat__button">Next</Button>
    </div>
  </div>
</template>

<script>
import Button from "./Button.vue";
export default {
  components: { Button },
};
</script>

<style lang="less" scoped>
.repeat {
  width: 100%;

  display: flex;
  flex-direction: column;
  align-items: center;

  &__image {
    display: block;

    width: 100%;
    max-width: 600px;

    border-radius: 10px;
  }
  &__buttons-wrapper {
    display: flex;
    gap: 20px;

    margin-top: 20px;
  }
  &__button {
    width: 100px;
  }

  &__wrapper {
    display: inline-block;
    perspective: 1000px;
  }
  .card {
    display: block;
    height: 100%;

    position: relative;

    cursor: pointer;
    transition-duration: 0.6s;
    transition-timing-function: ease-in-out;
    transform-style: preserve-3d;

    border-radius: 10px;

    box-shadow: hsl(206 22% 7% / 35%) 0px 10px 38px -10px,
      hsl(206 22% 7% / 20%) 0px 10px 20px -15px;
  }
  .card .back {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    backface-visibility: hidden;
    display: flex;
    justify-content: center;
    align-items: center;

    border-radius: 10px;

    font-size: 1.5rem;
    color: var(--text-color);
    background-color: var(--background-color);
    border: 3px solid var(--primary-color);
    
    display: flex;
    flex-direction: column;
  }

  .flip-left .card .back {
    transform: rotateY(-180deg);
  }

  .flip-left:hover .card {
    transform: rotateY(-180deg);
  }
}
</style>