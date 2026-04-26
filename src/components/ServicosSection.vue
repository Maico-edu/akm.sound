<template>
  <section id="servicos">
    <div class="slabel">O que fazemos</div>
    <h2>Serviços</h2>
    <div class="srv-grid">
      <div class="srv" v-for="s in servicos" :key="s.nome">
        <div class="srv-ic">{{ s.ic }}</div>
        <div class="srv-name">{{ s.nome }}</div>
        <div class="srv-desc">{{ s.desc }}</div>
      </div>
    </div>
  </section>
</template>

<script setup>
const servicos = [
  { ic: '🔊', nome: 'Instalação de Som',        desc: 'Centrais multimídia, subwoofers, tweeters e amplificadores.' },
  { ic: '🔧', nome: 'Conserto de Módulos',       desc: 'Diagnóstico e reparo de módulos de todas as marcas.' },
  { ic: '🎤', nome: 'Conserto de Alto-Falantes', desc: 'Recone, suspensão e reparo de falantes danificados.' },
  { ic: '📻', nome: 'Central Multimídia',        desc: 'Instalação de centrais Android, CarPlay e AndroidAuto.' },
  { ic: '⚡', nome: 'Elétrica Automotiva',       desc: 'Cabeamento, capacitores e baterias auxiliares.' },
  { ic: '🛠️', nome: 'Acessórios',                desc: 'Cabos RCA, fusíveis, terminais e mais.' },
]
</script>

<style scoped>
section {
  padding: 55px 6%;
  border-bottom: 1px solid var(--border);
  background: #0f1014;
}

.slabel {
  font-size: .65rem;
  font-weight: 700;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: var(--red);
  margin-bottom: .4rem;
}

h2 {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 2rem;
  color: #fff;
  letter-spacing: 1px;
  margin-bottom: 1.8rem;
}

.srv-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(190px, 1fr));
  gap: 1px;
  background: var(--border);
  border: 1px solid var(--border);
}

.srv {
  background: var(--card);
  padding: 1.4rem 1.2rem;
  transition: background .2s;
}
.srv:hover { background: #1a1d24; }

.srv-ic { font-size: 1.5rem; margin-bottom: .6rem; }
.srv-name { font-weight: 700; font-size: .88rem; color: #fff; margin-bottom: .35rem; }
.srv-desc { font-size: .8rem; color: var(--muted); line-height: 1.5; }
</style>