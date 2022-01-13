<template>
  <div class="app">
    <card-slide class="app__main"/>
  </div>
</template>

<script>
import CardSlide from "./components/molecules/card-slide";

export default {
  name: 'App',
  components: {
    CardSlide,
  }
}
</script>

<style lang="scss">
.app {
  display: grid;
  grid-template-rows: 100rem 1fr 100rem;
  grid-template-columns: 1fr;
  grid-template-areas:
    "header-unit"
    "main"
    "footer-item";
  height: 70vh;
  background-color: #fff9f9;
  background-image: url("./assets/images/icons/pattern-bg.svg");
  background-position: top center;
  background-size: 320rem;
  background-repeat: no-repeat;

  @include media('>=600') {
    grid-template-rows: 30rem 700rem 1fr;
    grid-template-columns: 1fr 80% 1fr;
    height: 100vh;

    background-position: top right;
    background-size: 700rem;
  }

  &__main {
    grid-area: main;
  }
}
</style>
