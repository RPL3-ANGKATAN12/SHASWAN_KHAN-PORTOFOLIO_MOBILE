<template>
  <SectionName :judul="judul">
    <a
      v-for="item in items"
      :key="item.id"
      :href="item.url"
      target="blank"
      class="border-t pt-4 flex items-center justify-between text-neutral-500 hover:text-black text-xl tracking-wide"
    >
      <span>{{ item.nama }}</span>
      <span>-></span>
    </a>
  </SectionName>
</template>

<script setup>
import SectionName from "./SectionName.vue";

defineProps({
  judul: {
    type: String,
    required: true,
  },
  items: {
    type: Array,
    required: true,
  },
});
</script>
