<template>
  <header class="w-full bg-white border-b border-neutral-300 top-0 fixed z-50">
    <div class="flex justify-between items-center px-8 py-2.5">
      <RouterLink to="/" class="font-bold text-xl">{{ judul }}</RouterLink>

      <slot />
    </div>
  </header>
</template>

<script setup>
defineProps({
  judul: {
    type: String,
    required: true
  }
})
</script>