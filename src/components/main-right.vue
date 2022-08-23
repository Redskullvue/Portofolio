<template>
  <div class="main-right">
    <h1 class="main-right--title">
      HI ! I Am
      <span class="main-right--title__header">Front-End</span>
      <br />Pooya Goodarzi
    </h1>
    <p class="main-right--desc">
      Front-End Vue js Developer for <b>1 year</b><br />
      and learning to be more.
    </p>
    <br />
    <div class="main-right--buttons">
      <button class="hire-me">Hire Me</button>
      <button class="projects">Projects</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "YMainRight",
};
</script>

<style lang="scss">
@import "@/assets/scss/variables";
.main-right {
  display: flex;
  justify-content: center;
  flex-direction: column;
  margin: 40px;
  &--title {
    width: 300px;
    font-size: 38px;
    &__header {
      font-size: 16px !important;
      background-color: rgb(76, 0, 255);
      color: $white;
      padding: 8px;
      border-radius: 10px;
    }
  }
  &--desc {
    margin-top: 40px;
    color: $secondery-text;
  }
  &--buttons {
    margin-top: 40px;
    .hire-me {
      padding: 15px 30px;
      background-color: $theme-color;
      color: $white;
      border: none;
      margin: 0px 30px;
      transition: 0.5s all;
      &:hover {
        background-color: $white;
        color: $theme-color;
        cursor: pointer;
      }
    }
    .projects {
      background-color: inherit;
      border: none;
      transition: 0.5s all;
      &:hover {
        color: $theme-color;
        cursor: pointer;
      }
    }
  }
}
</style>
