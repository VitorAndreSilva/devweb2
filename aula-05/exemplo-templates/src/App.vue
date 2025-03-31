<script setup>
  const nome = "João";
  const idade = 25;
  function inverter(texto) {
    return texto.split('').reverse().join('').toLowerCase();
  }
  function saudacao(nome) {
    return `Olá, mundo, ${nome}!`;
  }
</script>

<template>
  <div class="info">
    <h1>Informações</h1>
    <p>Nome: {{ nome }}</p>
    <p>Idade: {{ idade }}</p>
    <hr>
    <p>Para completar 50 anos: {{ 50 - idade }}</p>
    <p>O nome possui {{ nome.lenght }} caracteres</p>
    <p>O nome invertido é {{ inverter(nome) }}</p>
    <hr>
    <h3>Saudação</h3>
    <p>{{ saudacao(nome) }}</p>
  </div>
</template>

<style scoped>
.info {
  background-color: #97CF57;
  padding: 20px 30px;
  color: #113620;
  border-radius: 10px;
  border: 3px solid #113620;
}

h1 {
  color: #113620;
  font-weight: bold;
  font-size: 1.5em;
}
</style>
