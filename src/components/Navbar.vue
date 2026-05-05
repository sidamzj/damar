<script setup>
import { ref } from 'vue'

const menuOpen = ref(false)
const navItems = [
  { label: 'Home', href: '#home' },
  { label: 'Produk', href: '#pricing' },
  { label: 'Keunggulan', href: '#footer' },
  { label: 'Tentang Kami', href: '#keunggulan' }
]

const toggleMenu = () => {
  menuOpen.value = !menuOpen.value
}
import searchIcon from '../assets/search.png'
</script>

<template>
  <header class="sticky top-0 z-50 bg-red-600/95 backdrop-blur-md border-b border-white/10 shadow-2xl shadow-red-900/20">
    <div class="mx-auto flex max-w-7xl flex-wrap items-center justify-between gap-4 px-4 py-4 sm:px-6 lg:px-1">
      <div class="flex items-center gap-3">
        <div class="flex h-12 w-30 items-center justify-center rounded-[10px] bg-white shadow-sm ring-1 ring-white/100">
          <img src="../assets/logo.png" alt="Logo" class="h-90 w-auto object-contain"  />
        </div>
        <nav class="hidden md:flex items-center gap-4">
          <a
            v-for="item in navItems"
            :key="item.label"
            :href="item.href"
            class="text-sm font-semibold uppercase tracking-[0.16em] text-white transition hover:text-white/80"
          >
            {{ item.label }}
          </a>
        </nav>
      </div>

      <div class="hidden lg:flex flex-1 items-center justify-center">
        <div class="relative w-full max-w-md">
          <img :src="searchIcon" alt="Search" class="pointer-events-none absolute left-4 top-1/2 -translate-y-1/2 h-5 w-5" />
          <input
            type="search"
            placeholder="Cari layanan"
            class="w-full rounded-full border border-white/20 bg-white/95 py-2 pl-12 pr-4 text-sm text-slate-900 outline-none shadow-sm transition focus:border-white focus:ring-2 focus:ring-white/30"
          />
        </div>
      </div>

      <div class="hidden lg:flex items-center gap-3">
        <a
          href="#daftar"
          class="inline-flex items-center justify-center rounded-full bg-white px-5 py-2 text-sm font-semibold text-red-600 transition hover:bg-white/90"
        >
          Daftar
        </a>
        <router-link
          to="/login"
          class="inline-flex items-center justify-center rounded-full border border-white/70 px-5 py-2 text-sm font-semibold text-white transition hover:bg-white/20"
        >
          Login
        </router-link>
      </div>

      <button
        type="button"
        class="inline-flex items-center justify-center rounded-full border border-white/30 bg-white/10 p-2 text-white transition hover:bg-white/20 md:hidden"
        @click="toggleMenu"
        aria-label="Toggle menu"
      >
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" class="h-6 w-6">
          <path fill="currentColor" d="M4 6h16M4 12h16M4 18h16" />
        </svg>
      </button>
    </div>

    <transition name="fade-slide">
      <div v-if="menuOpen" class="border-t border-white/10 bg-red-600/95 md:hidden">
        <div class="mx-auto flex max-w-7xl flex-col gap-4 px-4 py-4 sm:px-6">
          <div class="relative rounded-full border border-white/20 bg-white/95 px-4 py-2 shadow-sm">
            <img :src="searchIcon" alt="Search" class="pointer-events-none absolute left-4 top-1/2 -translate-y-1/2 h-5 w-5" />
            <input
              type="search"
              placeholder="Cari layanan"
              class="w-full bg-transparent pl-12 pr-4 text-sm text-slate-900 outline-none"
            />
          </div>

          <div class="grid gap-2 rounded-3xl bg-white/10 p-3 text-white ring-1 ring-white/10">
            <a
              v-for="item in navItems"
              :key="item.label"
              :href="item.href"
              class="block rounded-full px-4 py-3 text-center text-sm font-semibold transition hover:bg-white/20"
            >
              {{ item.label }}
            </a>
          </div>

          <div class="grid gap-3 sm:grid-cols-2">
            <a
              href="#daftar"
              class="inline-flex items-center justify-center rounded-full bg-white px-5 py-3 text-sm font-semibold text-red-600 transition hover:bg-white/90"
            >
              Daftar
            </a>
            <router-link
              to="/login"
              class="inline-flex items-center justify-center rounded-full border border-white/60 bg-white/10 px-5 py-3 text-sm font-semibold text-white transition hover:bg-white/20"
            >
              Login
            </router-link>
          </div>
        </div>
      </div>
    </transition>
  </header>
</template>
