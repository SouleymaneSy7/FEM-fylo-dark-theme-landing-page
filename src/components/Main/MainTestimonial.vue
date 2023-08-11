<template>
  <section class="testimonial-container | container">
    <img class="quote" src="../../assets/bg-quotes.png" alt="Quotes Icon" />

    <div
      class="testimonial__card"
      v-for="testimonial in testimonialDetails"
      :key="testimonial.id"
    >
      <p class="base__font">{{ testimonial.testimonialText }}</p>

      <div class="profile">
        <div class="profile__img">
          <img :src="testimonial.profileImg" alt="Human picture" />
        </div>

        <div>
          <p class="sm__font fw-bold text-clr-900">
            {{ testimonial.profileName }}
          </p>
          <p class="sm__font">{{ testimonial.profileStatus }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from "vue";
import profileImg1 from "../../assets/profile-1.jpg";
import profileImg2 from "../../assets/profile-2.jpg";
import profileImg3 from "../../assets/profile-3.jpg";

const testimonialDetails = ref([
  {
    id: 0,
    testimonialText:
      "Fylo has improved our team productivity by an order of magnitude. Since making the switch our team has become a well-oiled collaboration machine.",
    profileImg: profileImg1,
    profileName: "Satish Patel",
    profileStatus: "Founder & CEO, Huddle",
  },
  {
    id: 1,
    testimonialText:
      "Fylo has improved our team productivity by an order of magnitude. Since making the switch our team has become a well-oiled collaboration machine.",
    profileImg: profileImg2,
    profileName: "Bruce McKenzie",
    profileStatus: "Founder & CEO, Huddle",
  },
  {
    id: 2,
    testimonialText:
      "Fylo has improved our team productivity by an order of magnitude. Since making the switch our team has become a well-oiled collaboration machine.",
    profileImg: profileImg3,
    profileName: "Iva Boyd",
    profileStatus: "Founder & CEO, Huddle",
  },
]);
</script>
