<template>
  <div class="app">
    <header-unit class="app__header-unit" />
    <ButtonUnit />

  </div>
</template>

<script>
import ButtonUnit from "./components/atoms/Button.vue";
import HeaderUnit from "./components/atoms/header-unit";

export default {
  name: 'App',
  components: {
    HeaderUnit,
    ButtonUnit,
  }
}
</script>

<style lang="scss">
.app {

  @include media('>=600') {
    display: grid;
    grid-template-rows: 100rem 1fr 100rem;
    grid-template-columns: 1fr;
    grid-template-areas:
    "header-unit"
    "main"
    "footer-unit";
  }

  &__header-unit {
    grid-area: header-unit;
  }
}
</style>
