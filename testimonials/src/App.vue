<template>
  <div class="app">
    <button-unit />
    <testimonial-unit />
  </div>
</template>

<script>
import ButtonUnit from "./components/atoms/button-unit";
import TestimonialUnit from "./components/atoms/testimonial-unit";

export default {
  name: 'App',
  components: {
    TestimonialUnit,
    ButtonUnit,
  }
}
</script>

<style lang="scss">
.app {
  background-color: aqua;
}
</style>
