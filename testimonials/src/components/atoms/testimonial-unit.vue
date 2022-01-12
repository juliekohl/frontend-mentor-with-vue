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
  position: relative;
  font: var(--font-inter);

  &::before {
    position: absolute;
    display: block;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 230rem;
    content: '';
    background-image: url(../../assets/images/icons/pattern-curve.svg);
    background-position: bottom left;
    background-repeat: no-repeat;
    background-size: 260rem;
  }

  &::after {
    position: absolute;
    display: block;
    top: 40rem;
    width: 100rem;
    height: 100rem;
    left: calc(50% - 50px);
    content: '';
    background-image: url("../../assets/images/icons/pattern-quotes.svg");
    background-position: top center;
    background-repeat: no-repeat;
    background-size: 60rem;
  }

  &__text {
    width: 90%;
    margin: 70rem auto 0;
    text-align: center;
    font-size: 18rem;
    font-weight: 300;
    color: var(--color-blue-100);
  }

  &__name {
    display: block;
    text-align: center;
    margin-top: 20rem;
    font-weight: 700;
    color: var(--color-blue-100);
  }

  &__job {
    display: block;
    text-align: center;
    margin-top: 5rem;
    font-size: 15rem;
    font-weight: 300;
    color: var(--color-gray-70);
  }
}
</style>
