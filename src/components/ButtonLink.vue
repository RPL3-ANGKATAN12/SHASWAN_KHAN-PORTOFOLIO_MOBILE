<template>
  <a
    v-if="link"
    :href="to"
    class="w-full text-center border border-black text-black px-8 py-3 uppercase tracking-wider hover:bg-black hover:text-white transition-colors duration-200"
  >
    {{ label }}
  </a>
  <RouterLink
    v-else
    :to="to"
    class="w-full text-center border border-black text-black px-8 py-3 uppercase tracking-wider hover:bg-black hover:text-white transition-colors duration-200"
  >
    {{ label }}
  </RouterLink>
</template>

<script setup>
defineProps({
  label: {
    type: String,
    required: true,
  },
  to: {
    type: String,
    required: false,
    default: "#",
  },
  link: {
    type: Boolean,
    required: true,
  },
});
</script>
