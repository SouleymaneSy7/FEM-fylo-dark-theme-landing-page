<template>
  <nav class="navbar | container">
    <a href="#" class="logo">
      <img src="../../assets/logo.svg" alt="Website Logo" />
    </a>

    <ul class="flex">
      <li v-for="link in headerLinks">
        <a href="#" class="link"> {{ link }} </a>
      </li>
    </ul>
  </nav>
</template>

<script setup>
import { ref } from "vue";
const headerLinks = ref(["Features", "Team", "Sign In"]);
</script>
