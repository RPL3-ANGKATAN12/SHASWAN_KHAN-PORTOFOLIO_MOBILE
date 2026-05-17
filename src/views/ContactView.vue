<template>
  <HeroSection class="pb-5" judul="Ayo membangun sesuatu bersama!" />

  <ContactMe judul="Email" :items="contactEmail" class="pb-0" />

  <ContactMe judul="Social Media" :items="socialMedia" />
</template>

<script setup>
import ContactMe from "@/components/ContactMe.vue";
import HeroSection from "@/components/HeroSection.vue";

const contactEmail = [
  {
    id: 1,
    nama: "example@gmail.com",
    url: "mailto:example@gmail.com"
  }
]

const socialMedia = [
  {
    id: 1,
    nama: "Github",
    url: "https://github.com/"
  },
  {
    id: 2,
    nama: "LinkedIn",
    url: "https://linkedin.com/"
  },
  {
    id: 3,
    nama: "Instagram",
    url: "https://instagram.com/"
  },
]
</script>
