<script setup>
import SubscribeForm from './components/SubscribeForm.vue';
</script>

<template>
  <main>
    <img src="./assets/images/logo.svg" alt="PING. - Logo" />

    <h1>We are launching <strong>soon!</strong></h1>

    <p>Subscribe and get notified</p>

    <SubscribeForm></SubscribeForm>

    <img id="dashboardIllustration" src="./assets/images/illustration-dashboard.png" alt="Dashboard illustration">

    <footer class="page-footer">
      <div class="social-button-container">
        <a class="social-button" href="/" aria-label="Facebook account">
          <img src="./assets/images/facebook-f-brands-solid-full.svg" alt="Facebook logo">
        </a>
        <a class="social-button" href="/" aria-label="Twitter account">
          <img src="./assets/images/twitter-brands-solid-full.svg" alt="Twitter logo">
        </a>
        <a class="social-button" href="/" aria-label="Instagram account">
          <img src="./assets/images/instagram-brands-solid-full.svg" alt="Instagram logo">
        </a>
      </div>

      <div class="footer-copy">
        <p>&copy; Copyright Ping. All rights reserved.</p>
        <p>
          Challenge by <a href="https://www.frontendmentor.io?ref=challenge">Frontend Mentor</a>.
          Coded by <a href="#">Jam954</a>.
        </p>
      </div>
    </footer>
  </main>
</template>

<style scoped>
.attribution {
  font-size: 0.6875rem;
  text-align: center;
}
.attribution a {
  color: hsl(228, 45%, 44%);
}
</style>
