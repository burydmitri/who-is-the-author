<template>
  <div class="cards">
    <CardWithPopover />
    <CardWithPopover />
    <CardWithPopover />
    <CardWithPopover />
    <CardWithPopover />

  </div>
</template>

<script>
import CardWithPopover from './CardWithPopover.vue'
export default {
    components: { CardWithPopover }
};
</script>

<style lang="less" scoped>
.cards {
    width: 100%;

    display: grid;
    gap: 10px;
    grid-template-columns: repeat(3, 1fr);
}
</style>