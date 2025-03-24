<script setup>
import { ref } from 'vue';

const contador = ref(0);

function incrementar() {
  contador.value++
}
function decrementar() {
  contador.value--
}

</script>

<template>
  <h1>Olá, mundo</h1>
  <div v-if="contador<=46">
    <p>Contador: {{ contador }}</p>
    <button @click="incrementar">+</button>
    <button @click="decrementar">-</button>
  </div>
  <div v-else="contador=46">
    <p>Contador: {{ contador }}</p>
    <p>Impossível incrementar</p>
    <button @click="decrementar">-</button>
  </div>
  
</template>

<style scoped>

</style>
