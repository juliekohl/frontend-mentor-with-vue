<template>
  <div class="img">
    <img
        class="img__photo"
        :src="require(`@/assets/images/${photo}.jpg`)"
        :alt="alt"
    />
    <button-unit class="img__button" />
  </div>
</template>

<script>
import ButtonUnit from "./button-unit";
export default {
  name: "image-unit",
  components: {ButtonUnit},
  props: {
    photo: String,
    alt: String
  }
}
</script>

<style lang="scss">
.img {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 300rem;
  padding: 10rem;

  &__photo {
    display: block;
    width: 250rem;
    margin: 230rem auto 0;
    box-shadow: var(--box-shadow-v2);

    @include media('>=600') {
      position: absolute;
      right: 60rem;
      max-width: 540rem;
      width: 55%;
      margin-top: 680rem;
    }
  }

  &__button {}
}
</style>
