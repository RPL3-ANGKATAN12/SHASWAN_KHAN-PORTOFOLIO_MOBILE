<script setup lang="ts">
import KotakHijau from "@/components/KotakHijau.vue";
import KotakKuning from "@/components/KotakKuning.vue";
import KotakMerah from "@/components/KotakMerah.vue";
</script>

<template>
  <div class="about">
    <h1>Halo 123</h1>
    <KotakMerah />
    <KotakKuning />
    <KotakHijau />
  </div>
</template>








<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
