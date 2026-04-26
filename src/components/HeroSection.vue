<template>
  <section id="hero">
    <div class="tag">Som Automotivo</div>
    <h1>AKM <span>SOUND</span></h1>
    <p class="desc">Instalação de som, conserto de módulos e alto-falantes, e acessórios para o seu carro.</p>
    <div class="btns">
      <a href="https://wa.me/5547972100079" target="_blank" class="btn-r">Pedir Orçamento</a>
      <a href="#servicos" class="btn-g">Ver Serviços</a>
    </div>
  </section>
</template>

<script setup>
</script>

<style scoped>
section {
  padding: 80px 6% 70px;
  border-bottom: 1px solid var(--border);
}

.tag {
  font-size: .68rem;
  font-weight: 700;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: var(--red);
  border: 1px solid var(--red);
  display: inline-block;
  padding: .2rem .7rem;
  margin-bottom: 1.2rem;
}

h1 {
  font-family: 'Bebas Neue', sans-serif;
  font-size: clamp(3.2rem, 9vw, 5.5rem);
  line-height: 1;
  color: #fff;
  letter-spacing: 2px;
  margin-bottom: 1rem;
}

h1 span { color: var(--red); }

.desc {
  font-size: .95rem;
  color: var(--muted);
  line-height: 1.75;
  max-width: 420px;
  margin-bottom: 2rem;
}

.btns { display: flex; gap: .7rem; flex-wrap: wrap; }

.btn-r {
  background: var(--red);
  color: #fff;
  font-weight: 700;
  font-size: .85rem;
  letter-spacing: 1px;
  text-transform: uppercase;
  padding: .7rem 1.6rem;
  border: none;
  cursor: pointer;
  display: inline-block;
}
.btn-r:hover { opacity: .85; }

.btn-g {
  background: transparent;
  color: var(--text);
  font-weight: 600;
  font-size: .85rem;
  letter-spacing: 1px;
  text-transform: uppercase;
  padding: .7rem 1.6rem;
  border: 1px solid var(--border);
  cursor: pointer;
  display: inline-block;
}
.btn-g:hover { border-color: var(--red); color: var(--red); }
</style>