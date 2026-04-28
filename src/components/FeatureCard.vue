<script setup>
defineProps({
  feature: Object,
})
</script>

<template>
  <article class="rounded-[2rem] bg-white p-6 shadow-xl">
    <div class="flex items-start gap-4">
      <div class="h-14 w-14 rounded-3xl bg-slate-200"></div>
      <div>
        <h3 class="text-lg font-semibold text-slate-900">{{ feature.title }}</h3>
        <p class="mt-3 text-sm leading-6 text-slate-600">{{ feature.description }}</p>
      </div>
    </div>
  </article>
</template>
