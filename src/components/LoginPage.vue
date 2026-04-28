<script setup>
import { ref } from 'vue'

const email = ref('')
const password = ref('')
const showPassword = ref(false)

const togglePassword = () => {
  showPassword.value = !showPassword.value
}
</script>

<template>
  <div class="grid min-h-screen lg:grid-cols-2">
    <div class="flex items-center justify-center bg-slate-50 px-6 py-12">
      <div class="w-full max-w-md rounded-[2rem] bg-white p-10 shadow-xl">
        <h1 class="text-3xl font-black text-slate-900">LOG IN</h1>
        <div class="mt-8 flex gap-4">
          <button class="h-12 w-12 rounded-3xl border border-slate-200 bg-white text-base font-semibold">G</button>
          <button class="h-12 w-12 rounded-3xl border border-slate-200 bg-white text-base font-semibold">F</button>
          <button class="h-12 w-12 rounded-3xl border border-slate-200 bg-white text-base font-semibold">GH</button>
        </div>
        <div class="my-8 h-px bg-slate-200"></div>
        <form class="grid gap-6">
          <label class="text-sm font-semibold text-slate-700">Email</label>
          <input type="email" v-model="email" placeholder="contohemail@gmail.com" class="w-full rounded-3xl border border-slate-200 bg-slate-50 px-5 py-4 text-sm text-slate-900 outline-none focus:border-red-500" />

          <label class="text-sm font-semibold text-slate-700">Password</label>
          <div class="flex items-center gap-3 rounded-3xl border border-slate-200 bg-slate-50 px-4 py-2">
            <input :type="showPassword ? 'text' : 'password'" v-model="password" placeholder="************" class="w-full bg-transparent text-sm text-slate-900 outline-none" />
            <button type="button" class="text-sm font-semibold text-red-600" @click="togglePassword">{{ showPassword ? 'Hide' : 'Show' }}</button>
          </div>

          <a href="#" class="text-sm font-medium text-red-600">Lupa Kata Sandi Anda?</a>
          <button type="button" class="rounded-full bg-red-600 px-5 py-4 text-sm font-semibold uppercase text-white shadow-lg shadow-red-600/20">LOGIN</button>
          <p class="text-sm text-slate-600">Belum Punya Akun ? <router-link to="/" class="font-semibold text-red-600">Daftar Sekarang</router-link></p>
        </form>
      </div>
    </div>

    <div class="relative flex items-center justify-center bg-red-500 px-6 py-12">
      <div class="absolute inset-0 bg-slate-200/40"></div>
      <div class="relative z-10 max-w-md text-center">
        <h2 class="text-4xl font-black text-slate-900">Welcome to FastNet</h2>
        <p class="mt-5 text-base text-slate-700">Internet cepat dan layanan lengkap dalam satu aplikasi.</p>
      </div>
    </div>
  </div>
</template>
