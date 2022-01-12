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
  background-color: white;
  //background-image: url(./src/assets/images/icons/pattern-bg.svg);
  background-position: top center;
  background-size: 320px;
  background-repeat: no-repeat;
  box-shadow: 0px 10px 18px 0px rgba(214, 214, 214, 0.5);

}
</style>
