<template>
  <div class="app">
    <button-unit />
  </div>
</template>

<script>
import ButtonUnit from "./components/atoms/button-unit";

export default {
  name: 'App',
  components: {
    ButtonUnit,
  }
}
</script>

<style lang="scss">
.app {
  background-color: aqua;
}
</style>
