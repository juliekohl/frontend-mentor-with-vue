<template>
  <a class="icon-unit" href="#" >
    <img
        class="icon-unit__image"
        :src="require(`@/assets/img/icons/${name}.svg`)"
        :alt="alt"
    />
  </a>

</template>

<script>
export default {
  name: "icon-unit",
  props: {
    name: String,
    alt: String
  },
}
</script>

<style lang="scss">

</style>