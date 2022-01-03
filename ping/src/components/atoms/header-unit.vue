<template>
  <div class="header-unit">
    <img
        class="header-unit__img"
        src="@/assets/img/icons/logo.svg"
        alt="logo"
    >
  </div>
</template>

<script>
export default {
  name: "header-unit"
}
</script>

<style lang="scss">
.header-unit {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  &__img {
    display: block;
    width: 110rem;
    margin: 150rem auto 0;

    @include media('>=600') {
      width: 90rem;
      margin: 155rem auto 0;
    }
  }
}
</style>
