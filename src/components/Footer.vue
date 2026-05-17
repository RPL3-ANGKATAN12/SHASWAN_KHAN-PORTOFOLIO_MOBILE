<template>
  <footer class="flex flex-col gap-8 py-2 justify-center items-center bg-white border-t border-neutral-300">
    <span class="font-bold text-xl">{{ judul }}</span>
    <div v-if="items" class="flex gap-3 text-sm">
      <a v-for="item in items" :key="item.id" :href="item.url" target="blank" class="underline underline-offset-2 font-medium text-neutral-500 hover:text-black">{{ item.nama }}</a>
    </div>
    <span class="text-neutral-500 text-sm tracking-wide">© 2026 {{ judul }}. All rights reserved.</span>
  </footer>
</template>

<script setup>
defineProps({
  judul: {
    type: String,
    required: true,
  },
  items: {
    type: Array,
    required: false
  }
})
</script>