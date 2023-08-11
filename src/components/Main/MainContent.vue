<template>
  <main class="main-container">
    <img
      class="bg-curvy"
      src="../../assets/bg-curvy-desktop.svg"
      alt="Curvy Background"
    />

    <MainCard />
    <MainDescription />
    <MainTestimonial />
    <MainForm />
  </main>
</template>

<script setup>
import MainCard from "./MainCard.vue";
import MainDescription from "./MainDescription.vue";
import MainForm from "./MainForm.vue";
import MainTestimonial from "./MainTestimonial.vue";
</script>
