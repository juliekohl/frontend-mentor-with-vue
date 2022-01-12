<template>
  <div class="app">
    <card-slide />
    <button-unit />
  </div>
</template>

<script>
import ButtonUnit from "./components/atoms/button-unit";
import CardSlide from "./components/molecules/card-slide";

export default {
  name: 'App',
  components: {
    CardSlide,
    ButtonUnit,
  }
}
</script>

<style lang="scss">
.app {
  display: grid;
  height: 70vh;
  background-color: #fff9f9;
  background-image: url("./assets/images/icons/pattern-bg.svg");
  background-position: top center;
  background-size: 320rem;
  background-repeat: no-repeat;

  @include media('>=600') {
    grid-template-columns: 1fr 330px 1fr;
    grid-template-rows: 1fr 650px 1fr;
    height: 100vh;
  }
}
</style>
