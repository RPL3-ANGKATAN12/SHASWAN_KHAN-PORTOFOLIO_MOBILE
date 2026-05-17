<template>
  <HeroSection
    judul="Membuat website dengan terampil dan sesuai standar"
    deskripsi="Lorem ipsum, dolor sit amet consectetur adipisicing elit. Provident perferendis repellendus ipsam eius omnis excepturi quibusdam deserunt dolorem soluta, voluptatum rerum temporibus reiciendis recusandae, earum doloribus nesciunt, vel debitis ullam!"
    :border-bottom="true"
  >
    <ButtonLink label="View Project" class="max-w-50" to="/project" :link="false" />
  </HeroSection>

  <!-- Bagian about -->
  <SectionName judul="about" :border-bottom="true">
    <p class="text-lg leading-relaxed">
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dignissimos
      tempora distinctio harum aut animi voluptatum ullam neque facere doloribus
      officiis minus dicta excepturi, ducimus modi voluptates facilis placeat
      unde laborum?
    </p>

    <!-- foto diri -->
    <div
      class="aspect-auto bg-neutral-300 w-full overflow-hidden rounded-lg mt-16"
    >
      <img
        src="@/assets/images/mrbeast.jpeg"
        class="w-full h-full object-cover"
        alt=""
      />
    </div>
  </SectionName>

  <!-- bagian skills -->
  <SectionName judul="skills">
    <SkillList :items="items" />
  </SectionName>
</template>

<script setup>
import ButtonLink from "@/components/ButtonLink.vue";
import HeroSection from "@/components/HeroSection.vue";
import SectionName from "@/components/SectionName.vue";
import SkillList from "@/components/SkillList.vue";

const items = [
  { id: 1, title: "Frontend", detail: "Vue / TailwindCss" },
  { id: 2, title: "Backend", detail: "Postgresql / Prisma" },
  { id: 3, title: "Sofware", detail: "Microsoft Office / Figma" },
];
</script>
