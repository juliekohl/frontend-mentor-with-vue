<template>
  <div class="testimonial">
    <p class="testimonial__text">
      <q
      >{{text}}</q
      >
    </p>
    <span class="testimonial__name">{{name}}</span>
    <span class="testimonial__job">{{job}}</span>
  </div>
</template>

<script>
export default {
  name: "testimonial-unit",
  props: {
    text: String,
    name: String,
    job: String
  }
}
</script>

<style lang="scss">
.testimonial {
  border: 2px solid green;
  &__text {
    width: 90%;
    margin: 70px auto 0;
    text-align: center;
    //margin-right: auto;
    font-size: 18px;
    font-weight: 300;
  }
  &__name {
    display: block;
    text-align: center;
    margin-top: 20px;
    font-weight: 700;
  }
  &__job {
    display: block;
    text-align: center;
    margin-top: 5px;
    font-size: 15px;
    font-weight: 300;
  }
}
</style>