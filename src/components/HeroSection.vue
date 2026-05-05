<script setup>
import homeImg from '../assets/home.png'
import appsIcon from '../assets/apps.png'
import playIcon from '../assets/play.png' 
</script>

<template>
  <section id="home" class="mx-auto max-w-7xl px-4 py-10 sm:px-6 lg:px-0.1">
    <div class="overflow-hidden rounded-[2rem] bg-gradient-to-r from-red-500 via-red-500 to-white-200 p-8 shadow-xl sm:p-12 lg:grid lg:grid-cols-[1.15fr_0.85fr] lg:items-center lg:gap-10">
      <div class="space-y-6 text-white">
        <h1 class="text-4xl font-black leading-tight sm:text-5xl lg:text-4xl">#FastNet FAST AT ANYTHING</h1>
        <p class="max-w-2xl font-semibold text-white/90 sm:text-lg lg:text-3xl">Jangan biarkan koneksi lambat menghambat aktivitasmu. Saatnya pindah ke yang lebih cepat!</p>
        <p class="text-white/85 lg:text-lg">Mulai dari beli paket internet sampai bayar tagihan, semua ada di aplikasi FastNetKu.</p>

        <div class="grid grid-cols-2 gap-2 w-max">
          <img :src="appsIcon" alt="Facebook" class="h-10 w-38 rounded-1xl " />
          <img :src="playIcon" alt="Google Play" class="h-10 w-38 rounded-1xl" />
        </div>
      </div>

      <div class="mt-10 lg:mt-0 flex flex-col items-center gap-4">
        <img :src="homeImg" alt="FastNet home hero" class="h-72 rounded-[2rem] object-cover sm:h-80" />
        <a href="#pricing" class="inline-flex items-center justify-center rounded-full px-8 py-4 text-sm font-semibold uppercase tracking-[0.12em] bg-red-600 px-5 py-3 text-sm font-semibold text-white shadow-lg shadow-red-600/20"">Pasang Sekarang</a>
      </div>
    </div>
  </section>
</template>
