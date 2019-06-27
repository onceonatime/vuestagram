<template>
  <nav class="TheBottom">
    <div class="TheBottom-ButtonGroup flexbox__between">
      <div class="TheBottom-Button col" v-for="(button,index) in buttons" :key="'button'+index">
        <i :class="button"></i>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "TheBottom",
  data() {
    return {
      buttons: [
        "fas fa-home",
        "fas fa-search",
        "far fa-plus-square",
        "far fa-heart",
        "far fa-user"
      ]
    };
  }
};
</script>

<style lang='scss' scoped>
@import "@/assets/css/index.scss";

.TheBottom {
  // size
  position: absolute;
  bottom: 0;
  // size
  width: 100%;
  // border
  border-top: 1px solid $border-color;
  // content
  background-color: $basic-bg-color;
  &-Button {
    // display
    display: flex;
    justify-content: center;
    align-items: center;
    // size
    width: 100%;
    height: 44px;
    // font
    font-size: 24px;
  }
}
</style>