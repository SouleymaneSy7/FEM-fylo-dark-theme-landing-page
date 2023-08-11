<template>
  <footer class="footer-container">
    <section class="container">
      <a href="#" class="logo">
        <img src="../../assets/logo.svg" alt="Website Logo" />
      </a>

      <section class="footer-flex">
        <div class="info">
          <img src="../../assets/icon-location.svg" alt="Location Svg Icon" />
          <p class="base__font">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua
          </p>
        </div>

        <section>
          <div class="info">
            <img src="../../assets/icon-phone.svg" alt="Phone Svg Icon" />
            <p class="base__font">+1-543-123-4567</p>
          </div>

          <div class="info">
            <img src="../../assets/icon-email.svg" alt="Email Svg Icon" />
            <p class="base__font">example@fylo.com</p>
          </div>
        </section>

        <nav>
          <ul>
            <li v-for="link in footerLinks1">
              <a href="#" class="link"> {{ link }} </a>
            </li>
          </ul>

          <ul>
            <li v-for="link in footerLinks2">
              <a href="#" class="link"> {{ link }} </a>
            </li>
          </ul>
        </nav>

        <section class="sci">
          <a href="#" class="sci__icon">
            <i class="fa-brands fa-facebook-f"></i>
          </a>

          <a href="#" class="sci__icon">
            <i class="fa-brands fa-twitter"></i>
          </a>

          <a href="#" class="sci__icon">
            <i class="fa-brands fa-instagram"></i>
          </a>
        </section>
      </section>

      <section class="attribution">
        <p>
          Challenge by
          <a href="https://www.frontendmentor.io?ref=challenge" target="_blank"
            >Frontend Mentor</a
          >
        </p>

        <p>
          Coded <span>&hearts;</span> by
          <a href="https://github.com/SouleymaneSy7" target="_blank"
            >Souleymane Sy</a
          >
        </p>
      </section>
    </section>
  </footer>
</template>

<script setup>
import { ref } from "vue";

const footerLinks1 = ref(["About Us", "Jobs", "Press", "Blog"]);
const footerLinks2 = ref(["Contact Us", "Terms", "Privacy"]);
</script>
