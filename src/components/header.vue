<template>
  <div class="header">
    <div class="header--title">
      <span>Pooya</span>
      <span class="header--title-dot">.</span>
    </div>
    <div class="header--items">
      <li v-for="btn in headerBtns" :key="headerBtns[btn]" class="header--item">
        {{ btn }}
      </li>
    </div>
    <div class="header--btn">
      <button class="header--chat-btn">Lets Chat</button>
    </div>
    <div @click="menu" class="header--btn--hamburger">
      <i class="fa fa-bars"></i>
    </div>
    <div class="responsive-menu" v-if="toggle">
      <li
        v-for="btn in headerBtns"
        :key="headerBtns[btn]"
        class="header--btn-responsive"
      >
        {{ btn }}
      </li>
    </div>
  </div>
</template>

<script>
export default {
  name: "YHeader",
  data() {
    return {
      toggle: false,
      headerBtns: ["Home", "Works", "About", "Projects"],
    };
  },
  methods: {
    menu() {
      // let resMenu = document.querySelector(".responsive-menu");
      if (!this.toggle) {
        this.toggle = true;
      } else if (this.toggle) {
        this.toggle = false;
      }
    },
  },
};
</script>

<style lang="scss">
@import "@/assets/scss/variables";
.header {
  display: grid;
  background-color: #fff;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: 80px;
  justify-items: center;
  align-items: center;
  border-bottom: 2px solid $primary-color;
  box-shadow: 1px 1px 10px $primary-color;
  &--title {
    font-size: 30px;
    font-weight: 900;
    margin-bottom: 2px;
    &-dot {
      color: $theme-color;
      font-size: 40px;
    }
  }
  &--item {
    display: inline;
    margin: 40px;
    transition: 0.5s all;
    &:hover {
      color: $theme-color;
      cursor: pointer;
    }
  }
  &--chat-btn {
    padding: 8px 16px;
    background-color: $white;
    transition: 0.5s all;
    &:hover {
      cursor: pointer;
      background-color: $theme-color;
      color: $white;
      border: 1px solid $white;
    }
  }
  .header--btn--hamburger {
    display: none;
  }
  .header--btn-responsive {
    margin: 14px 0px;
    list-style: none;
    &:hover {
      color: $theme-color;
    }
  }
}
@media screen and (max-width: 710px) {
  .header--items {
    display: none;
  }
  .header--btn {
    display: none;
  }
  .header--btn--hamburger {
    grid-column: 3/4;
    font-size: 25px;
    display: inline !important;
    &:hover {
      color: $theme-color;
    }
  }
}
</style>
