<template>
  <ul class="footer-item">
    <li class="footer-item__list">
      <icon-unit
          class="footer-item__icon"
          name="facebook-icon"
          alt="facebook icon"
      />
    </li>
    <li class="footer-item__list">
      <icon-unit
          class="footer-item__icon"
          name="twitter-icon"
          alt="twitter icon"
      />
    </li>
    <li class="footer-item__list">
      <icon-unit
          class="footer-item__icon"
          name="instagram-icon"
          alt="instagram icon"
      />
    </li>
  </ul>
  <p class="footer-item__paragraph">&copy; Copyright Ping. All rights reserved.</p>
</template>

<script>
import IconUnit from "../atoms/icon-unit";
export default {
  name: "footer-item",
  components: {IconUnit}
}
</script>

<style lang="scss">
.footer-item {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  width: 235rem;
  margin: 50rem auto 0;
  padding: 0;

  &__list {
    align-self: center;
    background-color: white;
    border: 1rem solid var(--color-gray-70);
    border-radius: 50%;

    &:hover {
      border-color: var(--color-blue-60);
      background: var(--color-blue-60);
    }
  }

  &__paragraph {
    margin: 50rem auto 30rem;
    text-align: center;
    font-size: 16rem;
    font-weight: 500;
    color: var(--color-gray-70);
  }
}
</style>
