<template>
  <img 
      class="photo" 
      :src="require(`@/assets/images/${photo}.jpg`)"
      :alt="alt"
  />
</template>

<script>
export default {
  name: "image-unit",
  props: {
    photo: String,
    alt: String
  }
}
</script>

<style lang="scss">
.photo {
  display: block;
  width: 250px;
  margin: 0 auto;
}
</style>