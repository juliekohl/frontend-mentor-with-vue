<template>
  <div class="app">
    <header-unit class="app__header-unit" />
    <section-form class="app__main" />
    <footer-item class="app__footer-item" />
  </div>
</template>

<script>
import HeaderUnit from "./components/atoms/header-unit";
import SectionForm from "./components/molecules/section-form";
import FooterItem from "./components/molecules/footer-item";

export default {
  name: 'App',
  components: {
    FooterItem,
    SectionForm,
    HeaderUnit,
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
    "footer-item";
  }

  &__header-unit {
    grid-area: header-unit;
  }

  &__main {
    grid-area: main;
  }

  &__footer-item {
    grid-area: footer-item;
  }
}
</style>
