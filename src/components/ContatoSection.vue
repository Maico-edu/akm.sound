<template>
  <section id="contato">
    <div class="slabel">Fale conosco</div>
    <h2>Contato</h2>
    <div class="contact-wrap">

      <div class="clinks">
        <a class="clink" href="https://wa.me/5547997210079" target="_blank">
          <span class="clink-ic">📲</span>
          <div>
            <div class="clink-lbl">WhatsApp</div>
            <div class="clink-val">+55 47 9721-0079</div>
          </div>
        </a>
        <a class="clink" href="https://www.instagram.com/akm_sound_" target="_blank">
          <span class="clink-ic">📸</span>
          <div>
            <div class="clink-lbl">Instagram</div>
            <div class="clink-val">@akm_sound_</div>
          </div>
        </a>
      </div>

      <div class="cform">
        <div class="frow">
          <div class="ff">
            <label>Nome</label>
            <input v-model="form.nome" placeholder="Seu nome" />
          </div>
          <div class="ff">
            <label>Telefone</label>
            <input v-model="form.tel" placeholder="(47) 9xxxx-xxxx" />
          </div>
        </div>
        <div class="ff">
          <label>Serviço</label>
          <select v-model="form.srv">
            <option value="">Selecione...</option>
            <option v-for="s in servicos" :key="s" :value="s">{{ s }}</option>
          </select>
        </div>
        <div class="ff">
          <label>Mensagem</label>
          <textarea v-model="form.msg" placeholder="Descreva o que precisa..."></textarea>
        </div>
        <button class="btn-r" @click="enviar">Enviar pelo WhatsApp</button>
      </div>

    </div>
  </section>
</template>

<script setup>
import { reactive } from 'vue'

const servicos = [
  'Instalação de Som',
  'Conserto de Módulos',
  'Conserto de Alto-Falantes',
  'Central Multimídia',
  'Elétrica Automotiva',
  'Acessórios',
]

const form = reactive({ nome: '', tel: '', srv: '', msg: '' })

function enviar() {
  const txt = `Olá AKM Sound! Meu nome é *${form.nome || 'cliente'}*${form.tel ? `, fone: ${form.tel}` : ''}.\nServiço: *${form.srv || 'Não informado'}*\n${form.msg}`
  window.open(`https://wa.me/5547997210079?text=${encodeURIComponent(txt)}`, '_blank')
}
</script>

<style scoped>
section {
  padding: 55px 6%;
  border-bottom: 1px solid var(--border);
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

.contact-wrap {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 2rem;
}
@media (max-width: 600px) { .contact-wrap { grid-template-columns: 1fr; } }

.clinks { display: flex; flex-direction: column; gap: .7rem; }

.clink {
  display: flex;
  align-items: center;
  gap: 1rem;
  background: var(--card);
  border: 1px solid var(--border);
  padding: 1rem 1.2rem;
  transition: border-color .2s;
}
.clink:hover { border-color: var(--red); }

.clink-ic { font-size: 1.3rem; }
.clink-lbl { font-size: .58rem; font-weight: 700; letter-spacing: 2px; text-transform: uppercase; color: var(--red); }
.clink-val { font-size: .88rem; color: var(--text); }

.cform { display: flex; flex-direction: column; gap: .65rem; }

.frow { display: grid; grid-template-columns: 1fr 1fr; gap: .65rem; }
@media (max-width: 420px) { .frow { grid-template-columns: 1fr; } }

.ff { display: flex; flex-direction: column; gap: .28rem; }
.ff label { font-size: .58rem; font-weight: 700; letter-spacing: 2px; text-transform: uppercase; color: var(--muted); }

.ff input,
.ff textarea,
.ff select {
  background: var(--card);
  border: 1px solid var(--border);
  color: var(--text);
  font-family: 'Exo 2', sans-serif;
  font-size: .88rem;
  padding: .58rem .85rem;
  outline: none;
  transition: border-color .2s;
  resize: none;
}
.ff input:focus,
.ff textarea:focus,
.ff select:focus { border-color: var(--red); }
.ff textarea { height: 95px; }
.ff select { cursor: pointer; appearance: none; }

.btn-r {
  width: 100%;
  background: var(--red);
  color: #fff;
  font-weight: 700;
  font-size: .85rem;
  letter-spacing: 1px;
  text-transform: uppercase;
  padding: .7rem 1.6rem;
  border: none;
  cursor: pointer;
}
.btn-r:hover { opacity: .85; }
</style>