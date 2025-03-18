<script setup>
  import { ref } from 'vue';

  const valor = ref(10); // objeto reativo
  const celsius = ref(0)
  const fahrenheit = ref(0);

  // function incrementar() {
  //   valor.value++ 
  // }

  function duplicar() {
    valor.value = valor.value * 2;
  }

  function toFahrenheit() {
    fahrenheit.value = (celsius.value * 9/5) + 32;
  }
</script>
<template>
  <h1>Hola, mondo!</h1>
  <button v-on:click="valor++">Incrementar</button>
  <!--<button v-on:click="incrementar">Incrementar</button>-->
  <button v-on:click="valor--">Decrementar</button>
  <button v-on:click="duplicar">Dobrar</button>
  <button v-on:click="valor=valor/2">Metadinha</button>
  <p>Valor: {{ valor }}</p>
  <hr>
  <input v-model="celsius" type="number" step="0.1" />
  <button v-on:click="toFahrenheit">Converter</button>
  <p>Temperatura em fahrenheit: {{ fahrenheit }}</p>
</template>
<style scoped>
  button {
    font-weight: bold;
    /*border: none;*/
    background-color: greenyellow;
  }
</style>