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
  display: flex;
  position: absolute;
  width: 80rem;
  height: 40rem;
  top: 265rem;
  left: calc(50% - 40rem);
  z-index: 1;

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
    box-shadow: 0rem 3rem 3rem 0rem rgba(214, 214, 214, 0.4);
  }

  &__btn-left {
    width: 40rem;
    background-repeat: no-repeat;
    background-position: center;
    background-color: white;
    background-size: 10rem;
    background-image: url(../../assets/images/icons/icon-prev.svg);
    border-radius: 50% 0 0 50%;
  }

  &__btn-right {
    width: 40rem;
    background-repeat: no-repeat;
    background-position: center;
    background-color: white;
    background-size: 10rem;
    background-image: url(../../assets/images/icons/icon-next.svg);
    border-radius: 0 50% 50% 0;
  }
}
</style>
