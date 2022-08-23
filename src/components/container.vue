<template>
  <div class="container">
    <div class="container--header"><y-header /></div>
    <div class="container--main"><y-main-right /></div>
  </div>
</template>

<script>
import YHeader from "./header.vue";
import YMainRight from "./main-right.vue";
export default {
  name: "YContainer",

  components: {
    YHeader,
    YMainRight,
  },
};
</script>

<style lang="scss">
@import "@/assets/scss/variables";
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  font-family: cursive;
}
.container {
  width: 100%;
  height: 100vh;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-template-rows: 80px 1fr;
  margin: 3px;
  &--header {
    grid-column: 1/-1;
  }
  &--main {
    grid-column: 1/2;
    grid-row: 2/3;
    padding: 30px;
    margin: 10px 120px;
  }
}
</style>
