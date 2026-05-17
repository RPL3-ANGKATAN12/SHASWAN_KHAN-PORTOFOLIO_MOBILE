<template>
  <HeroSection class="pb-7" judul="Projects" deskripsi="Lorem, ipsum dolor sit amet consectetur adipisicing elit. Officia at amet quod quidem. Tempore?" />

  <ProjectList :items="items" />
</template>

<script setup>
import HeroSection from '@/components/HeroSection.vue';
import ProjectList from '@/components/ProjectList.vue';

const items = [
  {
    id: 1,
    judul: "Dragon Ball Wiki",
    deskripsi: "lorem ipsum si amet dolor lorem ipsum si amet dolor lorem ipsum si amet dolor lorem ipsum si amet dolor.",
    gambar: "dragon-ball-wiki.png",
    teknologi: [
      {id: 1, nama: "Nuxt"},
      {id: 2, nama: "TypeScript"},
      {id: 3, nama: "REST API"},
      {id: 4, nama: "Nuxt UI"},
    ],
    link: "https://test-fetch-pi.vercel.app/"
  },
  {
    id: 2,
    judul: "Web Gallery",
    deskripsi: "lorem ipsum si amet dolor lorem ipsum si amet dolor lorem ipsum si amet dolor lorem ipsum si amet dolor.",
    gambar: "gallery-web.png",
    teknologi: [
      {id: 1, nama: "Vue"},
      {id: 2, nama: "JavaScript"},
      {id: 3, nama: "TailwindCss"},
    ],
    link: "https://github.com"
  },
  {
    id: 3,
    judul: "Web Travel",
    deskripsi: "lorem ipsum si amet dolor lorem ipsum si amet dolor lorem ipsum si amet dolor lorem ipsum si amet dolor.",
    gambar: "tampilan-web2.PNG",
    teknologi: [
      {id: 1, nama: "Nuxt"},
      {id: 2, nama: "Nuxt UI"},
      {id: 3, nama: "TypeScript"},
    ],
    link: "https://github.com"
  },
]
</script>