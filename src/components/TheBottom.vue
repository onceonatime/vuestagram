<template>
  <nav class="TheBottom">
    <div class="TheBottom-ButtonGroup" v-for="(button,index) in buttons" :key="'button'+index">
      <div class="TheBottom-Button">
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
.TheBottom {
  position: absolute;
  bottom: 0;
}
</style>