<script setup>
import { ref } from 'vue';

  const numero = ref(0);
  const selecionado = ref(0);
  const resultado = ref(0);
</script>
<template>
  <input v-model="numero" type="number">
  <input v-model="selecionado" type="number">
  <button v-on:click="resultado = numero * selecionado">=</button>
  <p>{{ resultado }}</p>
  <button>+</button><button>-</button><button>*</button><button>/</button>
</template>
<style scoped>
  p {
    border: 1px solid black;
  }
</style>