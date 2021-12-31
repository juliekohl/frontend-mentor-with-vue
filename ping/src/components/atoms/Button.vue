<template>
  <button class="button-unit">Notify Me</button>
</template>

<script>
export default {
  name: "ButtonUnit"
}
</script>

<style lang="scss">
.button-unit {
  width: 100%;
  height: 75rem;
  padding: 10rem;
  margin: 10rem;
  font-size: 25rem;
  font-weight: 600;
  text-align: center;
  color: white;
  background-color: var(--color-blue-60);
  border-radius: 45rem;

  @include media('>=600') {
    width: 200rem;
    height: 55rem;
    font-size: 16rem;
  }
}
</style>
