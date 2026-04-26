<template>
  <NavBar />
  <HeroSection />
  <ServicosSection />
  <ContatoSection />
  <FooterSection />
  <a class="wa" href="https://wa.me/5547972100079?text=Olá%20AKM%20Sound!%20Gostaria%20de%20um%20orçamento." target="_blank">📲</a>
</template>

<script setup>
import NavBar from './components/NavBar.vue'
import HeroSection from './components/HeroSection.vue'
import ServicosSection from './components/ServicosSection.vue'
import ContatoSection from './components/ContatoSection.vue'
import FooterSection from './components/FooterSection.vue'
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Exo+2:wght@400;600;700&display=swap');

*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

:root {
  --red: #e81c2e;
  --dark: #0c0d10;
  --card: #13151a;
  --border: #22252e;
  --text: #c8cad4;
  --muted: #5a5e70;
}

body {
  font-family: 'Exo 2', sans-serif;
  background: var(--dark);
  color: var(--text);
}

a { text-decoration: none; color: inherit; }

::-webkit-scrollbar { width: 4px; }
::-webkit-scrollbar-thumb { background: var(--red); }

.wa {
  position: fixed; bottom: 1.4rem; right: 1.4rem; z-index: 99;
  width: 50px; height: 50px; border-radius: 50%;
  background: #25d366;
  display: flex; align-items: center; justify-content: center;
  font-size: 1.4rem;
  box-shadow: 0 4px 14px rgba(37,211,102,.35);
  transition: transform .2s;
}
.wa:hover { transform: scale(1.1); }
</style>