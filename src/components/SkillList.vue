<template>
  <div class="flex flex-col border-t border-neutral-400">
    <div
      v-for="item in items"
      :key="item.id"
      class="py-2 border-b border-neutral-400 flex justify-between items-center hover:border-black transition-colors duration-200 group"
    >
      <!-- ini title skill -->
      <span class="text-lg leading-normal font-medium">{{ item.title }}</span>

      <!-- ini detail skill nya -->
      <span
        class="border border-neutral-300 text-neutral-500 px-3 py-1 text-xs leading-none tracking-widest font-semibold group-hover:text-black group-hover:border-neutral-500 transition-colors duration-200"
        >{{ item.detail }}</span
      >
    </div>
  </div>
</template>

<script setup>
defineProps({
  items: {
    type: Array,
    required: true,
  },
});
</script>
