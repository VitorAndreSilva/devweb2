<script setup>
  import { ref } from 'vue';

  const newsletter = ref([
    {
      id: 1,
      title: "Mochila roubada no IFC",
      date: "03/04/2025",
      font: "www.araquarinews.com.br",
      address: "http://localhost:5173",
      subject: "Mochila roubada na biblioteca do IFC - Campus Araquari às 2h da manhã. Pais do aluno acionam a instituição na  justiça diante da omissão por parte da mesma."
    },
    {
      id: 2,
      title: "Mochila roubada no IFC",
      date: "04/04/2025",
      font: "www.araquarinews.com.br",
      address: "http://localhost:5173",
      subject: "Mochila roubada na biblioteca do IFC - Campus Araquari às 3h da manhã. Pais do aluno acionam a instituição na  justiça diante da omissão por parte da mesma."
    },
    {
      id: 3,
      title: "Mochila roubada no IFC",
      date: "05/04/2025",
      font: "www.araquarinews.com.br",
      address: "http://localhost:5173",
      subject: "Mochila roubada na biblioteca do IFC - Campus Araquari às 4h da manhã. Pais do aluno acionam a instituição na  justiça diante da omissão por parte da mesma."
    },
    {
      id: 4,
      title: "Mochila roubada no IFC",
      date: "06/04/2025",
      font: "www.araquarinews.com.br",
      address: "http://localhost:5173",
      subject: "Mochila roubada na biblioteca do IFC - Campus Araquari às 5h da manhã. Pais do aluno acionam a instituição na  justiça diante da omissão por parte da mesma."
    },
    {
      id: 5,
      title: "Mochila roubada no IFC",
      date: "07/04/2025",
      font: "www.araquarinews.com.br",
      address: "http://localhost:5173",
      subject: "Mochila roubada na biblioteca do IFC - Campus Araquari às 6h da manhã. Pais do aluno acionam a instituição na  justiça diante da omissão por parte da mesma."
    }
  ])
</script>
<template>
  <h1>IFLetter</h1>
  <div class="news">
    <ul>
      <li v-for="(news, id) in newsletter" :key="id">
        {{ news.title }} | {{ news.date }}<br>
        {{ news.subject }}<br>
        Fonte: {{ news.font }}<br>
        Link para o mesmo: <a>{{ news.address }}</a>
      </li>
    </ul>
  </div>
</template>
<style scoped>

</style>