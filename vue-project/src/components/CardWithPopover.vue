<template>
  <PopoverRoot>
    <PopoverTrigger>
      <Card />
    </PopoverTrigger>
    <PopoverPortal>
      <PopoverContent :side-offset="5" class="popover__content" side="bottom">
        <img
          class="popover__image"
          src="https://d7hftxdivxxvm.cloudfront.net/?height=334&quality=80&resize_to=fill&src=https%3A%2F%2Fartsy-media-uploads.s3.amazonaws.com%2FDX2ifF8rooHgPwQk2ADNdA%252FEmergingMag.png&width=445"
          alt=""
        />
        <h2 class="popover__author">Joe Cadoe</h2>
        <p class="popover__name">"Spirit of nature"</p>
        <Button>Add to repeat</Button>
        <PopoverArrow class="popover__arrow" />
      </PopoverContent>
    </PopoverPortal>
  </PopoverRoot>
</template>

<script>
import Card from "./Card.vue";
import Button from "./Button.vue"
import {
  PopoverAnchor,
  PopoverArrow,
  PopoverClose,
  PopoverContent,
  PopoverPortal,
  PopoverRoot,
  PopoverTrigger,
} from "radix-vue";

export default {
  components: {
    Card,
    Button,
    PopoverAnchor,
    PopoverArrow,
    PopoverClose,
    PopoverContent,
    PopoverPortal,
    PopoverRoot,
    PopoverTrigger,
  },
};
</script>

<style lang="less" >
.popover {
  &__content {
    border-radius: 4px;
    padding: 20px;
    width: 30vw;
    background-color: var(--background-color);
    box-shadow: hsl(206 22% 7% / 35%) 0px 10px 38px -10px,
      hsl(206 22% 7% / 20%) 0px 10px 20px -15px;
    animation-duration: 400ms;
    animation-timing-function: cubic-bezier(0.16, 1, 0.3, 1);
    will-change: transform, opacity;

    // &:focus {
    //   box-shadow: hsl(206 22% 7% / 35%) 0px 10px 38px -10px,
    //     hsl(206 22% 7% / 20%) 0px 10px 20px -15px, 0 0 0 2px var(--grass-7);
    // }

    &[data-state="open"][data-side="top"] {
      animation-name: slideDownAndFade;
    }
    &[data-state="open"][data-side="right"] {
      animation-name: slideLeftAndFade;
    }
    &[data-state="open"][data-side="bottom"] {
      animation-name: slideUpAndFade;
    }
    &[data-state="open"][data-side="left"] {
      animation-name: slideRightAndFade;
    }
  }
  &__arrow {
    fill: white;
  }
  &__image {
    width: 100%;
    border-radius: 4px;
  }
  &__name {
    margin-bottom: 10px;
  }
}

@keyframes slideUpAndFade {
  from {
    opacity: 0;
    transform: translateY(2px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes slideRightAndFade {
  from {
    opacity: 0;
    transform: translateX(-2px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes slideDownAndFade {
  from {
    opacity: 0;
    transform: translateY(-2px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes slideLeftAndFade {
  from {
    opacity: 0;
    transform: translateX(2px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}
</style>