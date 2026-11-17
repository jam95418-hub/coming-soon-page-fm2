<script setup>
import { ref } from 'vue';

const emailInput = ref(null);
const hasInvalidEmail = ref(false);

function validateEmail() {
  hasInvalidEmail.value = !emailInput.value.checkValidity();
}

function clearErrorWhenValid() {
  if (emailInput.value.validity.valid) {
    hasInvalidEmail.value = false;
  }
}
</script>

<template>
  <form class="subscribe-form" @submit.prevent="validateEmail">
    <div class="email-field">
      <input
        ref="emailInput"
        type="email"
        name="email"
        class="email-input"
        :class="{ 'email-input--invalid': hasInvalidEmail }"
        :aria-invalid="hasInvalidEmail"
        :aria-describedby="hasInvalidEmail ? 'email-error' : undefined"
        aria-label="Email"
        placeholder="Your email address..."
        required
        @input="clearErrorWhenValid"
      />
      <p v-if="hasInvalidEmail" id="email-error" class="email-error" role="alert">
        Please provide a valid email address
      </p>
    </div>
    <button type="button" class="notify-button" @click="validateEmail">Notify Me</button>
  </form>
</template>