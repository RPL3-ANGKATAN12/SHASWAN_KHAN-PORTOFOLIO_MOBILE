<template>
  <Header>
    <template v-slot:kiri>
      <RouterLink to="/" class="font-bold text-xl">Portofolio</RouterLink>
    </template>
    <!-- button toggle sidebar -->
     <template v-slot:kanan>
      <button class="hover:bg-neutral-200 px-2 py-1" @click="toggleSideBar">
        {{ openSideBar ? "Close" : "Menu" }}
      </button>
    </template>
  </Header>

  <SideBar v-model="openSideBar" :items="sideBarItems" />

  <main class="pt-13 min-h-screen px-8 mx-auto">
    <RouterView />
  </main>

  <Footer judul="Portofolio" :items="footerItems" />
</template>

<script setup>
import { ref } from "vue";
import { RouterLink, RouterView } from "vue-router";
import SideBar from "./components/SideBar.vue";
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";

const openSideBar = ref(false);

function toggleSideBar() {
  openSideBar.value = !openSideBar.value;
}

const sideBarItems = [
  {
    id: 1,
    nama: "Home",
    to: "/"
  },
  {
    id: 2,
    nama: "Project",
    to: "/project"
  },
  {
    id: 3,
    nama: "Contact",
    to: "/contact"
  },
]

const footerItems = [
  {
    id: 1,
    nama: "Github",
    url: "https://github.com/"
  },
  {
    id: 2,
    nama: "LinkedInd",
    url: "https://linkedin.com/"
  },
  {
    id: 3,
    nama: "Instagram",
    url: "https://instagram.com/"
  },
]
</script>
