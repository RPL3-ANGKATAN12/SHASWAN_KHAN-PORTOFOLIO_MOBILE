<template>
  <section
    class="py-16 flex flex-col gap-2"
    :class="borderBottom ? 'border-b border-neutral-300' : ''"
  >
    <h2
      v-if="judul"
      class="text-sm font-medium text-neutral-500 uppercase tracking-widest"
    >
      {{ judul }}
    </h2>

    <slot />
  </section>
</template>

<script setup>
defineProps({
  judul: {
    type: String,
    required: false,
  },
  borderBottom: {
    type: Boolean,
    required: false,
  },
});
</script>
