<template>
  <section class="form-container">
    <h3 class="third-title fw-bold text-clr-900">Get early access today</h3>
    <p class="base__font">
      It only takes a minute to sign up and our free starter tier is extremely
      generous. If you have any questions, our support team would be happy to
      help you.
    </p>

    <form class="form" @submit.prevent="formSubmit()">
      <label for="email">
        <input
          type="email"
          name="email"
          id="email"
          placeholder="email@example.com"
          class="input"
          v-model="inputValue"
          @input="formSubmit()"
        />

        <span class="errors | sm__font" v-if="inputError">
          {{ Errors }}
        </span>
      </label>
      <button type="submit" class="btn">Get Started For Free</button>
    </form>
  </section>
</template>

<script setup>
import { ref } from "vue";

const Errors = ref("Please enter a valid email address");
const inputValue = ref("");
const inputError = ref(false);
const regEx = /^([a-z\d\.-]+)@([a-z\d-]+)\.([a-z]{2,8})(\.[a-z]{2,8})?$/;

const formSubmit = () => {
  if (regEx.test(inputValue.value)) {
    inputError.value = false;
  } else {
    inputError.value = true;
  }
};
</script>
