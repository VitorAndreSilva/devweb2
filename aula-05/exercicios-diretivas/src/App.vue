<script setup>
  import { ref } from "vue";

  const nome = "Vitor";
  const idade = 16;
  function inverter(texto) {
    return texto.split('').reverse().join('').toUpperCase();
  }
  function saudacao(nome) {
    return `Olá, mundo, ${nome}!`;
  }
  const contador = ref(0);
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
  <div class="contador">
    <button @click="contador++">+</button>
    <button @click="contador--">-</button>
    <div v-if="contador<10" class="vermelha">
      <p>Contador = {{ contador }}</p>
    </div>
    <div v-else class="verde">
      <p>Contador = {{ contador }}</p>
    </div>
  </div>
</template>

<style scoped>
.info,
  .contador {
    background-color: #97CF57;
    padding: 20px 30px;
    color: #113620;
    border-radius: 10px;
  }

  h1 {
    color: #113620;
    font-weight: bold;
    font-size: 1.5em;
  }

  button {
    margin: 10px;
    padding: 10px;
    border: 0;
    border-radius: 5px;
    background-color: lightblue;
    color: #113620;
    font-weight: bold;
    cursor: pointer;
  }

  button:hover {
    background-color: #113620;
    color: #97CF57;
  }

  div {
    margin: 10px 0;
    padding: 10px;
    border-radius: 5px;
    color: #113620;
    font-weight: bold;
  }

  .vermelha {
    background-color: rgb(223, 81, 81);
  }
</style>
