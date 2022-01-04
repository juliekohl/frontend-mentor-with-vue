<template>
  <div class="section-form">
    <Form
        class="section-form__form"
        @submit="onSubmit"
        :validation-schema="schema"
    >
      <div class="section-form__header">
        <h1 class="section-form__heading">We are launching <strong>soon!</strong></h1>
        <p class="section-form__paragraph">Subscribe and get notified</p>
      </div>
      <Field
          class="section-form__input"
          placeholder="Your email address..."
          type="email"
          id="email"
          name="email"
      />
      <ErrorMessage
          class="section-form__span"
          name="email"
      />
      <button-unit class="section-form__button" type="submit" />
    </Form>
    <div class="section-form__image">
      <img
          class="section-form__img"
          src="@/assets/img/illustration-dashboard.png"
          alt="illustration"
      >
    </div>
  </div>
</template>

<script>
import ButtonUnit from "../atoms/button-unit";
import { Form, Field, ErrorMessage } from "vee-validate";
import * as yup from 'yup';

export default {
  name: "section-form",
  components: { ButtonUnit, Form, Field, ErrorMessage },
  data() {
    const schema = yup.object({
      email: yup.string().required().email().label('Email'),
    });
    return {
      schema,
    };
  },
  methods: {
    onSubmit(values) {
      console.log(1, values);
      location.reload();
    },
  },
}
</script>

<style lang="scss">
.section-form {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 95vw;
  margin: 0 auto;

  &__header {
    margin: 20rem;
    font-size: var(--font-primary);
  }

  &__heading {
    margin-top: 80rem;
    text-align: center;
    font-weight: 300;
    font-size: 27rem;
    color: var(--color-gray-70);

    @include media('>=420') {
      font-size: 33rem;
    }

    @include media('>=600') {
      font-size: 50rem;
    }

    @include media('>=1024') {
      margin-top: 90rem;
      font-size: 55rem;
    }
  }

  strong {
    font-weight: 700;
    color: var(--color-blue-100);
  }

  &__paragraph {
    margin-top: 25rem;
    text-align: center;
    font-size: 16rem;

    @include media('>=420') {
      font-size: 20rem;
    }

    @include media('>=600') {
      font-size: 25rem;
    }

    @include media('>=1024') {
      margin-top: 20rem;
      font-size: 20rem;
    }
  }

  &__input {
    width: 100%;
    margin-top: 30rem;
    padding: 15rem;
    text-align: center;
    font-size: 22rem;
    border: 1rem solid var(--color-gray-70);
    border-radius: 40px;
    color: var(--gray);

    @include media('>=600') {
      width: 60%;
      margin-right: 10rem;
    }
  }

  &__span {
    display: block;
    width: 200rem;
    margin-top: 10rem;
    text-align: start;
    color: var(--color-red-40);
  }

  &__image {
    @include media('>=600') {
      --width-max: 900rem;
    }
  }

  &__img {
    display: block;
    width: 100%;
    margin: 65rem auto;
  }
}
</style>
