<script setup>
import fbIcon from '../assets/f.png'
import xIcon from '../assets/x.png'
import youtubeIcon from '../assets/youtube.png'
import igIcon from '../assets/ig.png'
import appsIcon from '../assets/apps.png'
import playIcon from '../assets/play.png' 
</script>

<template>
  <section id="footer">
  <footer class="bg-gradient-to-r from-red-600 via-red-500 to-pink-500 text-white">
    <div class="mx-auto grid max-w-7xl gap-40 px-4 py-16 sm:px-6 lg:grid-cols-4 lg:px-8">
      <div class="space-y-6">
        <h3 class="text-lg font-semibold">Download App</h3>
        <p class="text-sm text-white/80">Download Sekarang:</p>
        <div class="flex gap-5">
          <img :src="appsIcon" alt="Facebook" class="h-10 w-38 rounded-1xl " />
          <img :src="playIcon" alt="Google Play" class="h-10 w-38 rounded-1xl" />
        </div>
        <div class="flex items-center gap-5">
          <img :src="fbIcon" alt="Facebook" class="h-10 w-10 rounded-2xl " />
          <img :src="xIcon" alt="X" class="h-10 w-10 rounded-2xl" />
          <img :src="youtubeIcon" alt="YouTube" class="h-10 w-10 rounded-2xl" />
          <img :src="igIcon" alt="Instagram" class="h-10 w-10 rounded-2xl" />
        </div>
      </div>

      <div>
        <h3 class="text-lg font-semibold">Layanan Digital</h3>
        <ul class="mt-4 space-y-3 text-sm text-white/90">
          <li>Video</li>
          <li>Games</li>
          <li>Music</li>
          <li>Aplikasi Kami</li>
        </ul>
      </div>

      <div>
        <h3 class="text-lg font-semibold">Jelajahi</h3>
        <ul class="mt-4 space-y-3 text-sm text-white/90">
          <li>Home</li>
          <li>Promo</li>
          <li>Keunggulan</li>
          <li>Produk</li>
        </ul>
      </div>

      <div>
        <h3 class="text-lg font-semibold">Bantuan</h3>
        <ul class="mt-4 space-y-3 text-sm text-white/90">
          <li>Pusat Bantuan</li>
          <li>Hubungi Kami</li>
          <li>Kendala Internet</li>
          <li>Lokasi FastNet Kami</li>
        </ul>
      </div>
    </div>
  </footer>
  </section>
</template>
