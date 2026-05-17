<template>
  <section
    class="py-16 flex flex-col gap-3"
    :class="borderBottom ? 'border-b border-neutral-300' : ''"
  >
    <h1
      class="text-5xl font-sans font-semibold text-black leading-tight tracking-tighter"
    >
      {{ judul }}
    </h1>
    <p
      v-if="deskripsi"
      class="text-lg leading-relaxed tracking-tight text-neutral-500 max-w-xl"
    >
      {{ deskripsi }}
    </p>
      <slot />
  </section>
</template>

<script setup>
defineProps({
  judul: {
    type: String,
    required: true,
  },
  deskripsi: {
    type: String,
    required: false,
  },
  borderBottom: {
    type: Boolean,
    required: false,
  },
});
</script>
