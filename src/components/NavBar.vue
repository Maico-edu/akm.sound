<template>
  <nav>
    <div class="logo">AKM<span>.</span>SOUND</div>
    <a href="https://wa.me/55479972100079" target="_blank">
      <button class="nav-btn">📲 WhatsApp</button>
    </a>
  </nav>
</template>

<script setup>
</script>

<style scoped>
nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 6%;
  height: 60px;
  border-bottom: 1px solid var(--border);
  position: sticky;
  top: 0;
  background: var(--dark);
  z-index: 99;
}

.logo {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 1.6rem;
  letter-spacing: 3px;
  color: #fff;
}

.logo span { color: var(--red); }

.nav-btn {
  background: var(--red);
  color: #fff;
  font-family: 'Exo 2', sans-serif;
  font-weight: 700;
  font-size: .78rem;
  letter-spacing: 1px;
  text-transform: uppercase;
  padding: .45rem 1.2rem;
  border: none;
  cursor: pointer;
}
</style>