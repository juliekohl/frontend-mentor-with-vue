<template>
  <a class="icon-unit" href="#" >
    <img
        :class="[
            'icon-unit__image',
            name && `icon-unit__image--name-${name}`
            ]"
        :src="require(`@/assets/img/icons/${name}.svg`)"
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
    color: var(--color-blue-60);

    &:hover {
      color: white;
    }

    &--name-facebook-icon {
      width: 15rem;
    }
    &--name-twitter-icon {
      width: 20rem;
    }
    &--name-instagram-icon {
      width: 23rem;
    }
  }
}
</style>
