<template>
  <a class="icon-unit" href="#" >
    <img
        :class="[
            'icon-unit__image',
            name && `icon-unit__image--name-${name}`
            ]"
        :alt="alt"
    />
  </a>
</template>

<script>
export default {
  name: "icon-unit",
  props: {
    name: {
      type: String,
      default: null,
      validator: (value) => {
        return ['facebook-icon', 'twitter-icon', 'instagram-icon'].includes(value);
      }
    },
    alt: String
  },
}
</script>

<style lang="scss">
.icon-unit {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  width: 35rem;
  height: 35rem;

  &__image {
    align-self: center;
    mask-repeat: no-repeat;
    mask-position: center center;
    background-color: var(--color-blue-60);

    &:hover {
      background-color: white;
    }

    &--name-facebook-icon {
      mask-image: url(../../assets/img/icons/facebook-icon.svg);
      mask-size: 15rem;
    }

    &--name-twitter-icon {
      mask-image: url(../../assets/img/icons/twitter-icon.svg);
      mask-size: 20rem;
    }

    &--name-instagram-icon {
      mask-image: url(../../assets/img/icons/instagram-icon.svg);
      mask-size: 23rem;
    }
  }
}
</style>
