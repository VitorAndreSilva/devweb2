<script setup>
  import { ref } from 'vue';

  const contador = ref(0);
</script>

<template>
  <div v-if="contador>=0 & contador<44">
    <h1>Contador de Aniversário</h1>
    <p>{{ contador }}</p>
    <button @click="contador++">+</button>
    <button @click="contador--">-</button>
  </div>
  <div v-else-if="contador<0">
    <h1>Contador de Aniversário</h1>
    <p>O contador não pode ser menor que 0</p>
    <button @click="contador++">+</button>
  </div>
  <div v-else-if="contador=44" class="parabens">
    <h1>Parabéns, mamãe!</h1>
    <p>{{ contador }} 🥳🥳🥳</p>
    <p>Deus abençoe muito a sua vida! Seu mini programador ama muito você! ❤️</p>
    <button @click="contador--">-</button>
  </div>
</template>

<style scoped>
  .parabens h1 {
    font-family: 'Times New Roman', Times, serif;
    color: rgb(219, 43, 43);
  }
  button {
    height: 2.5vw;
    width: 2.5vw;
  }
</style>
