<script setup>
import PricingCard from './PricingCard.vue'

const plans = [
  {
    label: 'HEMAT 20%',
    name: 'THR - 100 Mbps Internet',
    speed: '75 Mbps',
    duration: '1 Bulan',
    price: 'Rp 175.000',
    features: ['Internet', 'Perangkat 7-9 Perangkat', 'Promo biaya pasang Rp 50.000', 'Benefit aplikasi streaming'],
  },
  {
    label: 'HEMAT 20%',
    name: 'THR - 150 Mbps Internet',
    speed: '100 Mbps',
    duration: '1 Bulan',
    price: 'Rp 203.000',
    features: ['Internet', 'Perangkat 11-12 Perangkat', 'Promo biaya pasang Rp 50.000', 'Benefit aplikasi streaming'],
  },
  {
    label: 'HEMAT 20%',
    name: 'THR - 100 Mbps Internet + MAXStreamTV',
    speed: '75 Mbps',
    duration: '1 Bulan',
    price: 'Rp 255.500',
    features: ['Internet', 'Perangkat 7-9 Perangkat', 'Promo biaya pasang Rp 50.000', 'Benefit TV Channel'],
  },
  {
    label: 'HEMAT 20%',
    name: 'THR - 150 Mbps Internet + MAXStreamTV',
    speed: '100 Mbps',
    duration: '1 Bulan',
    price: 'Rp 283.500',
    features: ['Internet', 'Perangkat 7-9 Perangkat', 'Promo biaya pasang Rp 50.000', 'Benefit TV Channel'],
  },
]
</script>

<template>
  <section id="pricing" class="mx-auto max-w-7xl px-4 py-14 sm:px-6 lg:px-8">
    <div class="mb-12 text-center">
      <h2 class="text-3xl font-black text-slate-900">Paket FastNet</h2>
      <p class="mx-auto mt-4 max-w-2xl text-sm text-slate-600">Pilih paket yang sesuai untuk rumah dan keluarga Anda.</p>
    </div>
    <div class="pricing-grid grid gap-6 lg:grid-cols-4">
      <PricingCard v-for="plan in plans" :key="plan.name" :plan="plan" />
    </div>
  </section>
</template>
