<template>
  <div class="button">
    <button class="button__btn-left"></button>
    <button class="button__btn-right"></button>
  </div>
</template>

<script>
export default {
  name: "button-unit"
}
</script>

<style lang="scss">
.button {
  position: absolute;
  top: 265rem;
  left: calc(50% - 40rem);
  z-index: 1;
  display: flex;
  width: 80rem;
  height: 40rem;
  border-radius: 50%;
  box-shadow: var(--box-shadow-v2);

  @include media('>=600') {
    top: 585rem;
    right: 410rem;
    left: auto;
    width: 120rem;
    height: 60rem;
  }

  &__btn {
    flex-grow: 1;
    width: 40rem;
    height: 40rem;
    background-repeat: no-repeat;
    background-position: center;
    background-color: white;
    background-size: 10rem;
    border: 0;
    cursor: pointer;
  }

  &__btn-left {
    width: 40rem;
    background-repeat: no-repeat;
    background-position: center;
    background-color: white;
    background-size: 10rem;
    background-image: url(../../assets/images/icons/icon-prev.svg);
    border-radius: 50% 0 0 50%;

    @include media('>=600') {
      width: 120rem;
      background-size: 12rem;
    }
  }

  &__btn-right {
    width: 40rem;
    background-repeat: no-repeat;
    background-position: center;
    background-color: white;
    background-size: 10rem;
    background-image: url(../../assets/images/icons/icon-next.svg);
    border-radius: 0 50% 50% 0;

    @include media('>=600') {
      width: 120rem;
      background-size: 12rem;
    }
  }

}
</style>
