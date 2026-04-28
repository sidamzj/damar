<script setup>
import Navbar from './Navbar.vue'
import HeroSection from './HeroSection.vue'
import PromoSection from './PromoSection.vue'
import KeunggulanSection from './KeunggulanSection.vue'
import PricingSection from './PricingSection.vue'
import FAQSection from './FAQSection.vue'
import Footer from './Footer.vue'
</script>

<template>
  <div>
    <Navbar />
    <main class="space-y-24">
      <HeroSection />
      <PromoSection />
      <KeunggulanSection />
      <PricingSection />
      <FAQSection />
    </main>
    <Footer />
  </div>
</template>
