<template>
  <div class="card-slide">
    <image-unit
        class="card-slide__image"
        photo="image-tanya"
        alt="image tanya"
    />
    <testimonial-unit
        class="card-slide__testimonial"
        text="I’ve been interested in coding for a while but never taken the jump until now. I couldn’t recommend this course enough. I’m now in the job of my dreams and so excited about the future."
        name="Tanya Sinclair"
        job="UX Engineer"
    />
  </div>
</template>

<script>
import ImageUnit from "../atoms/image-unit";
import TestimonialUnit from "../atoms/testimonial-unit";
export default {
  name: "card-slide",
  components: {TestimonialUnit, ImageUnit}
}
</script>

<style lang="scss">
.card-slide {
  display: contents;
  border: 2px solid blue;
  width: 100%;
  margin-top: 35px;
  opacity: 0;

  &.active {
    left: 0;
    opacity: 1;
    transition: 0.5s;
  }

  &.prev-active {
    left: -50%;
    transform: rotate(-10deg);
    transition: 1s;
  }

  &.next-active {
    left: 50%;
    transform: rotate(10deg);
    transition: 1s;
  }

  &__image {}

  &__testimonial {}
}
</style>