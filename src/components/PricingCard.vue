<script setup>
defineProps({
  plan: Object,
})
</script>

<template>
  <article class="flex h-full flex-col justify-between rounded-[2rem] bg-white p-6 shadow-xl">
    <div>
      <span class="inline-flex rounded-full bg-red-50 px-3 py-1 text-[0.72rem] font-semibold uppercase tracking-[0.2em] text-red-600">{{ plan.label }}</span>
      <h3 class="mt-5 text-lg font-semibold text-slate-900">{{ plan.name }}</h3>
      <p class="mt-4 text-3xl font-black text-slate-900">{{ plan.speed }} <span class="text-base font-medium text-slate-500">| {{ plan.duration }}</span></p>
      <ul class="mt-6 space-y-3 text-sm text-slate-600">
        <li v-for="feature in plan.features" :key="feature" class="flex items-start gap-3">
          <span class="mt-2 inline-flex h-2.5 w-2.5 rounded-full bg-red-600"></span>
          <span>{{ feature }}</span>
        </li>
      </ul>
    </div>
    <div class="mt-6 flex flex-col gap-4">
      <div class="text-2xl font-black text-slate-900">{{ plan.price }}</div>
      <button class="rounded-full bg-red-600 px-5 py-3 text-sm font-semibold text-white shadow-lg shadow-red-600/20">Langganan</button>
    </div>
  </article>
</template>
