<template>
  <section class="card-container container">
    <div class="card" v-for="card in cardDetails" :key="card.id">
      <img :src="card.cardImg" alt="Illustration Svg" />

      <h3 class="card__title | fw-bold text-clr-900">{{ card.cardTitle }}</h3>

      <p class="base__font">{{ card.cardText }}</p>
    </div>
  </section>
</template>

<script setup>
// Imports
import { ref } from "vue";
import cardImg1 from "../../assets/icon-access-anywhere.svg";
import cardImg2 from "../../assets/icon-security.svg";
import cardImg3 from "../../assets/icon-collaboration.svg";
import cardImg4 from "../../assets/icon-any-file.svg";

const cardDetails = ref([
  {
    id: 0,
    cardImg: cardImg1,
    cardTitle: "Access your files, anywhere",
    cardText:
      "The ability to use a smartphone, tablet, or computer to access your account means your files follow you everywhere.",
  },
  {
    id: 1,
    cardImg: cardImg2,
    cardTitle: "Security you can trust",
    cardText:
      "2-factor authentication and user-controlled encryption are just a couple of the security features we allow to help secure your files.",
  },
  {
    id: 2,
    cardImg: cardImg3,
    cardTitle: "Real-time collaboration",
    cardText:
      "Securely share files and folders with friends, family and colleagues for live collaboration. No email attachments required.",
  },
  {
    id: 3,
    cardImg: cardImg4,
    cardTitle: "Store any type of file",
    cardText:
      "Whether you're sharing holidays photos or work documents, Fylo has you covered allowing for all file types to be securely stored and shared.",
  },
]);
</script>
