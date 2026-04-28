<script setup>
import FeatureCard from './FeatureCard.vue'

const features = [
  {
    title: 'Internet cepat',
    description: 'Kecepatan hingga 300 Mbps untuk streaming dan gaming.',
  },
  {
    title: 'Hiburan lengkap',
    description: 'Akses konten streaming dan TV on demand.',
  },
  {
    title: 'Paket lengkap',
    description: 'Semua layanan dalam satu paket mudah.',
  },
  {
    title: 'Layanan bantuan',
    description: 'Bantuan 24/7 melalui call center dan chat.',
  },
]
</script>

<template>
  <section id="tentang" class="mx-auto max-w-7xl px-4 py-14 sm:px-6 lg:px-8">
    <div class="mb-12 text-center">
      <h2 class="text-3xl font-black text-slate-900">Keunggulan FastNet Untuk Kebutuhan Digital Keluarga</h2>
      <p class="mx-auto mt-4 max-w-2xl text-sm text-slate-600">Internet cepat, hiburan lengkap, gaming lancar, dan bantuan layanan setiap saat.</p>
    </div>
    <div class="feature-grid grid gap-6 lg:grid-cols-4">
      <FeatureCard v-for="feature in features" :key="feature.title" :feature="feature" />
    </div>
  </section>
</template>
