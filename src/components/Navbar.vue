<script setup>
import { ref } from 'vue'

const menuOpen = ref(false)
const navItems = [
  { label: 'Home', href: '#home' },
  { label: 'Produk', href: '#produk' },
  { label: 'Tentang Kami', href: '#tentang' },
  { label: 'Keunggulan', href: '#keunggulan' }
]

const toggleMenu = () => {
  menuOpen.value = !menuOpen.value
}
</script>

<template>
  <header class="sticky top-0 z-50 bg-red-600/95 backdrop-blur-md border-b border-white/10 shadow-2xl shadow-red-900/20">
    <div class="mx-auto flex max-w-7xl flex-wrap items-center justify-between gap-4 px-4 py-4 sm:px-6 lg:px-8">
      <div class="flex items-center gap-3">
        <div class="flex h-15 w-27 items-center justify-center rounded-[25px] bg-white shadow-sm ring-2 ring-white/40">
          <img src="../assets/logo.png" alt="Logo" class="h-10 w-auto object-contain" />
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
          <span class="pointer-events-none absolute left-4 top-1/2 -translate-y-1/2 text-slate-400">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" class="h-5 w-5">
              <path fill="currentColor" d="M10 2a8 8 0 1 1 0 16 8 8 0 0 1 0-16Zm0 2a6 6 0 1 0 0 12 6 6 0 0 0 0-12Zm8.707 13.293-4.829-4.829A5.963 5.963 0 0 0 16 10a6 6 0 1 0-2 4.586l4.829 4.829a1 1 0 0 0 1.414-1.414Z"/>
            </svg>
          </span>
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
            <span class="pointer-events-none absolute left-4 top-1/2 -translate-y-1/2 text-slate-500">
              <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" class="h-5 w-5">
                <path fill="currentColor" d="M10 2a8 8 0 1 1 0 16 8 8 0 0 1 0-16Zm0 2a6 6 0 1 0 0 12 6 6 0 0 0 0-12Zm8.707 13.293-4.829-4.829A5.963 5.963 0 0 0 16 10a6 6 0 1 0-2 4.586l4.829 4.829a1 1 0 0 0 1.414-1.414Z"/>
              </svg>
            </span>
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
