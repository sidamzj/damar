<script setup>
import PromoCard from './PromoCard.vue'

const promos = [
  {
    label: 'IndiHome',
    title: '75Mbps + Netflix',
    description: 'Dunia Bajak Laut, Serunya Berlanjut.',
  },
  {
    label: 'IndiHome',
    title: '75Mbps + Netflix',
    description: 'Dapatkan paket internet lengkap dan hiburan.',
  },
  {
    label: 'Promo Ramadan',
    title: 'IndiHome',
    description: 'Promo spesial bundel internet dan MAXStreamTV.',
  },
]
</script>

<template>
  <section id="produk" class="mx-auto max-w-7xl px-4 py-14 sm:px-6 lg:px-8">
    <div class="mb-10">
      <h2 class="text-3xl font-black text-slate-900">Promo</h2>
    </div>
    <div class="promo-list grid gap-6 lg:grid-cols-3">
      <PromoCard v-for="promo in promos" :key="promo.title + promo.label" :promo="promo" />
    </div>
  </section>
</template>
