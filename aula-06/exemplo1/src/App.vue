<script setup lang="ts">
    import { ref } from "vue";

    let contador1 = ref(0);
    let contador2 = ref(0);
    let boolean = ref(true);
    console.log(boolean.value);

    function somar() {
        return contador1.value + contador2.value;
    }

    function inverter() {
        boolean.value == !boolean.value;
    }
</script>

<template>
  <div class="contadores">
    <div>
        <p>{{ contador1 }}</p>
        <button @click="contador1++">+</button>
        <button @click="contador1--">-</button>
    </div>
    <div>
        <p>{{ contador2 }}</p>
        <button @click="contador2++">+</button>
        <button @click="contador2--">-</button>
    </div>
  </div>
  <div>
    <div class="soma">
        <p>{{ somar() }}</p>
    </div>
    <div v-if="somar() > 10">
        <p>Maior que 10</p>
    </div>
    <div v-else-if="somar() == 10">
        <p>Igual a 10</p>
    </div>
    <div v-else>
        <p>Menor que 10</p>
    </div>
    <div v-if="somar() % 2 == 0">
        <p>Número par</p>
    </div>
    <div v-else>
        <p>Número ímpar</p>
    </div>
  </div>
  <div class="booleano">
    <div v-if="boolean">
        <p>Verdadeiro</p>
    </div>
    <div v-else>
        <p>Falso</p>
    </div>
    <button @click="inverter()">Inverter</button>
  </div>
</template>

<style scoped>

</style>
