<script setup>
import heroImg from '../assets/hero.png'
</script>

<template>
  <div class="site-shell">
    <header class="site-header">
      <div class="top-nav">
        <div class="brand">
          
        </div>

        <nav class="nav-links">
          <a href="#home">HOME</a>
          <a href="#produk">PRODUK</a>
          <a href="#tentang">TENTANG KAMI</a>
        </nav>

        <button class="login-btn">LOG IN</button>
      </div>
    </header>

    <main class="page-content">
      <section class="hero-section" id="home">
        <div class="hero-copy">
        
          <h1>FAST AT ANYTHING</h1>
          <p class="hero-text">Jangan biarkan koneksi lambat menghambat aktivitasmu. Saatnya pindah ke yang lebih cepat!</p>
          <p class="hero-note">Mulai dari beli paket internet sampai bayar tagihan, semua ada di aplikasi FastNetKu.</p>

          <div class="hero-actions">
            <a href="#order" class="btn btn-primary">PASANG SEKARANG</a>
            <div class="download-group">
              <a href="#appstore" class="store-btn store-app">
                <span>Download on the</span>
                <strong>App Store</strong>
              </a>
              <a href="#playstore" class="store-btn store-play">
                <span>GET IT ON</span>
                <strong>Google Play</strong>
              </a>
            </div>
          </div>
        </div>

        <div class="hero-media">
          <img :src="heroImg" alt="FastNet user enjoying connectivity" />
        </div>
      </section>

      <section class="promo-section" id="produk">
        <h2>Promo</h2>
        <div class="promo-grid">
          <article class="promo-card promo-card-soft">
            <div class="promo-top">
              <span class="promo-chip">IndiHome</span>
              <span class="promo-speed">75Mbps + Netflix</span>
            </div>
            <div class="promo-copy">
              <p>Dunia Bajak Laut, Serunya Berlanjut. Langganan Netflix di IndiHome Sekarang!</p>
            </div>
            <div class="promo-meta">
              <strong>Rp 280rb / bulan</strong>
              <span>Biaya pasang baru cuma Rp 50 ribu</span>
            </div>
          </article>

          <article class="promo-card promo-card-soft">
            <div class="promo-top">
              <span class="promo-chip">IndiHome</span>
              <span class="promo-speed">75Mbps + Netflix</span>
            </div>
            <div class="promo-copy">
              <p>Dunia Bajak Laut, Serunya Berlanjut. Langganan Netflix di IndiHome Sekarang!</p>
            </div>
            <div class="promo-meta">
              <strong>Rp 280rb / bulan</strong>
              <span>Biaya pasang baru cuma Rp 50 ribu</span>
            </div>
          </article>

          <article class="promo-card promo-card-strong">
            <div class="promo-top">
              <span class="promo-chip">Promo Ramadan</span>
              <span class="promo-speed">IndiHome</span>
            </div>
            <div class="promo-copy">
              <p>Internet + Movie Netflix mulai dari 75Mbps hanya Rp 280rb/bulan. Spesial saldo GoPay hingga Rp 150 ribu.</p>
            </div>
            <div class="promo-meta">
              <strong>Rp 150rb - Rp 385rb / bulan</strong>
              <span>Promo terbatas untuk pengguna baru dan Halo.</span>
            </div>
          </article>
        </div>
      </section>
    </main>
  </div>
</template>
