<template>
  <SectionName class="pt-0 gap-6">
    <article
      v-for="item in items"
      :key="item.id"
      class="border border-neutral-300 bg-white overflow-hidden"
    >
      <div v-if="item.gambar" class="aspect-video w-full overflow-hidden">
        <img
          :src="ambilGambar(item.gambar)"
          class="w-full h-full object-cover"
          alt=""
        />
      </div>

      <div class="p-6 space-y-4">
        <h2 class="text-2xl font-medium leading-tight tracking-tight">
          {{ item.judul }}
        </h2>
        <p class="text-[16px] text-neutral-500">
          {{ item.deskripsi }}
        </p>
        <div class="flex flex-wrap gap-2">
          <span
            v-for="teknologi in item.teknologi"
            :key="teknologi.id"
            class="px-2 py-0.5 border border-neutral-500 text-sm leading-none tracking-widest text-neutral-500 uppercase"
            >{{ teknologi.nama }}</span
          >
        </div>
        <div class="flex">
          <ButtonLink label="View Project ->" :to="item.link" :link="true" />
        </div>
      </div>
    </article>
  </SectionName>
</template>

<script setup>
import ButtonLink from "./ButtonLink.vue";
import SectionName from "./SectionName.vue";

defineProps({
  items: {
    type: Array,
    required: true,
  },
});

function ambilGambar(namaGambar) {
  return new URL(`../assets/images/project/${namaGambar}`, import.meta.url).href;
}
</script>
