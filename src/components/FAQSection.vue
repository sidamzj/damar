<script setup>
import { ref } from 'vue'

const faqs = [
  {
    question: 'Apa itu FastNet?',
    answer: 'FastNet adalah penyedia internet cepat dengan paket lengkap untuk rumah dan bisnis.',
  },
  {
    question: 'Apa saja Add-on?',
    answer: 'Add-on meliputi layanan tambahan seperti MAXStreamTV, kuota extra, dan dukungan premium.',
  },
  {
    question: 'Bagaimana cara registrasi FastNet?',
    answer: 'Registrasi dapat dilakukan melalui aplikasi FastNetKu atau dengan mendaftar online di halaman FastNet.',
  },
]

const openIndex = ref(0)

const toggle = (index) => {
  openIndex.value = openIndex.value === index ? -1 : index
}
</script>

<template>
  <section class="mx-auto max-w-7xl px-4 py-14 sm:px-6 lg:px-8">
    <div class="mb-12 text-center">
      <h2 class="text-3xl font-black text-slate-900">Tanya Jawab</h2>
      <p class="mx-auto mt-4 max-w-2xl text-sm text-slate-600">Pertanyaan umum tentang FastNet dan layanan kami.</p>
    </div>
    <div class="faq-list grid gap-4">
      <div v-for="(item, index) in faqs" :key="item.question" class="overflow-hidden rounded-[2rem] bg-white shadow-xl">
        <button class="flex w-full items-center justify-between px-6 py-5 text-left text-lg font-semibold text-slate-900" type="button" @click="toggle(index)">
          <span>{{ item.question }}</span>
          <span class="text-2xl text-red-600">{{ openIndex === index ? '-' : '+' }}</span>
        </button>
        <div v-show="openIndex === index" class="border-t border-slate-200 px-6 py-4 text-slate-600">
          <p>{{ item.answer }}</p>
        </div>
      </div>
    </div>
  </section>
</template>
