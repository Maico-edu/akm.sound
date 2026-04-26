<template>
  <footer>
    <div class="f-logo">AKM<span>.</span>SOUND</div>
    <div class="f-copy">© 2025 AKM Sound</div>
    <a class="f-ig" href="https://www.instagram.com/akm_sound_" target="_blank">@akm_sound_</a>
  </footer>
</template>

<script setup>
</script>

<style scoped>
footer {
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 1rem;
  padding: 1.4rem 6%;
}

.f-logo {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 1.2rem;
  letter-spacing: 2px;
  color: #fff;
}
.f-logo span { color: var(--red); }

.f-copy { font-size: .72rem; color: var(--muted); }

.f-ig {
  font-size: .72rem;
  font-weight: 700;
  letter-spacing: 1px;
  color: var(--red);
}
</style>