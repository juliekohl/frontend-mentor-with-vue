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
      <button-unit class="section-form__button"/>
    </Form>
  </div>
</template>

<script>
import ButtonUnit from "../atoms/Button";
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
  }
  strong {
    font-weight: 700;
    color: var(--color-blue-100);
  }

  &__paragraph {
    margin-top: 25rem;
    text-align: center;
    font-size: 16rem;
  }

  &__input {
    width: 100%;
    margin-top: 30rem;
    padding: 20rem;
    text-align: center;
    font-size: 22rem;
    border: 1rem solid var(--color-gray-70);
    border-radius: 40px;
    color: var(--gray);
  }
  &__span {
    color: var(--color-red-40);
  }
}
</style>
