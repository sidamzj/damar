<script setup>
defineProps({
  promo: Object,
})
</script>

<template>
  <article class="overflow-hidden rounded-[2rem] bg-slate-950 text-white shadow-xl">
    <img :src="promo.image" alt="Promo" class="h-50 w-full object-cover" />
    <div class="relative p-5">
      <span class="inline-flex rounded-full bg-white/15 px-3 py-1 text-xs font-semibold uppercase tracking-[0.16em]">{{ promo.label }}</span>
      <h3 class="mt-4 text-xl font-semibold">{{ promo.title }}</h3>
      <p class="mt-3 text-sm leading-6 text-slate-200">{{ promo.description }}</p>
    </div>
  </article>
</template>
