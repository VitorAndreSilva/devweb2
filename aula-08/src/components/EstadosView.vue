<script setup>
  import { ref } from "vue";

    const estados = ref([
    'São Paulo',
    'Rio de Janeiro',
    'Belo Horizonte',
    'Salvador',
    'Fortaleza',
    'Curitiba',
    'Manaus',
    'Recife',
    'Porto Alegre',
    'Brasília',
    ]);

    const estadosOrdenados = estados.value.sort()
</script>
<template>
    <div>
        <ul>
            <li v-for="estado in estadosOrdenados" :key="estado">
                {{ estado }}
            </li>
        </ul>
    </div>
</template>
<style scoped></style>