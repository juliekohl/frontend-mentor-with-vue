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
  width: 100%;
  margin-top: 35rem;
  padding: 10rem;
  font: var(--font-inter);

  @include media('>=600') {
    position: absolute;
    top: 160rem;
    left: 90rem;
    z-index: 1;
    display: flex;
    flex-wrap: wrap;
    width: 40%;
  }

  &::before {
    position: absolute;
    display: block;
    top: 320rem;
    left: 0;
    width: 100%;
    height: 230rem;
    content: '';
    background-image: url(../../assets/images/icons/pattern-curve.svg);
    background-position: bottom left;
    background-repeat: no-repeat;
    background-size: 260rem;

    @include media('>=600') {
      bottom: 0;
      height: 300rem;
      background-size: 480rem;
    }
  }

  &::after {
    position: absolute;
    display: block;
    top: 210rem;
    width: 100rem;
    height: 100rem;
    left: calc(50% - 50px);
    content: '';
    background-image: url("../../assets/images/icons/pattern-quotes.svg");
    background-position: top center;
    background-repeat: no-repeat;
    background-size: 60rem;

    @include media('>=600') {
      top: 0rem;
      left: 50rem;
      width: 140rem;
      height: 140rem;
      background-position: top left;
      background-size: 140rem;
    }
  }

  &__text {
    width: 90%;
    margin: 240rem auto 0;
    text-align: center;
    font-size: 18rem;
    font-weight: 300;
    color: var(--color-blue-100);

    @include media('>=600') {
      width: auto;
      margin-top: 0;
      font-size: 32rem;
      text-align: left;
      line-height: 43rem;
    }
  }

  &__name {
    display: block;
    text-align: center;
    margin-top: 20rem;
    font-weight: 700;
    color: var(--color-blue-100);

    @include media('>=600') {
      margin-top: 40rem;
      font-size: 20rem;
    }
  }

  &__job {
    display: block;
    text-align: center;
    margin-top: 5rem;
    font-size: 15rem;
    font-weight: 300;
    color: var(--color-gray-70);

    @include media('>=600') {
      margin-top: 40rem;
      margin-left: 20rem;
      font-size: 20rem;
    }
  }
}
</style>
