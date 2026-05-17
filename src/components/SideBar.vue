<template>
<!-- Overlay gelap di belakang sidebar -->
  <div
    v-if="open"
    class="fixed inset-0 bg-black/30 z-30"
    @click="open = false"
  />

  <!-- Sidebar -->
  <aside
    :class="open ? 'translate-x-0' : '-translate-x-full'"
    class="fixed top-0 left-0 w-64 h-screen flex flex-col gap-2 bg-neutral-50 px-3 py-2.5 z-40 transition-transform duration-300 pt-16"
  >
    <RouterLink
      v-for="item in items"
      :key="item.id"
      class="hover:bg-neutral-200 px-1.5 py-1"
      active-class="font-bold bg-neutral-200"
      :to="item.to"
      @click="open = false"
      >{{ item.nama }}</RouterLink
    >
  </aside>
</template>

<script setup>
const open = defineModel({default: false})
defineProps({
  items: {
    type: Array,
    required: false,
  }
})
</script>