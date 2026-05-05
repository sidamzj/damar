<script setup>
import PromoCard from './PromoCard.vue'
import promo1 from '../assets/promo1.png'
import promo2 from '../assets/promo2.png'
import promo3 from '../assets/promo3.png'

const promos = [
  {
    label: 'IndiHome',
    title: '75Mbps + Netflix',
    description: 'Dunia Bajak Laut, Serunya Berlanjut.',
    image: promo1,
  },
  {
    label: 'IndiHome',
    title: '75Mbps + Netflix',
    description: 'Dapatkan paket internet lengkap dan hiburan.',
    image: promo2,
  },
  {
    label: 'Promo Ramadan',
    title: 'IndiHome',
    description: 'Promo spesial bundel internet dan MAXStreamTV.',
    image: promo3,
  },
]
</script>

<template>
  <section id="produk" class="mx-auto max-w-7xl px-4 py-14 sm:px-6 lg:px-8">
    <div class="mb-10 text-center">
      <h2 class="text-3xl font-black text-slate-900" >Promo</h2>
    </div>
    <div class="promo-list grid gap-6 lg:grid-cols-3">
      <PromoCard v-for="promo in promos" :key="promo.title + promo.label" :promo="promo" />
    </div>
  </section>
</template>
