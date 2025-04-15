<script setup>
  import { ref } from 'vue';

  const newsletter = ref([
    {
      id: 1,
      cover: "https://noticias.memoria.araquari.ifc.edu.br/wp-content/uploads/sites/11/2016/12/IMG_0841-300x169.jpg",
      title: "Mochila roubada no IFC",
      date: "03/04/2025",
      font: "www.araquarinews.com.br",
      address: "http://localhost:5173",
      subject: "Mochila roubada na biblioteca do IFC - Campus Araquari às 2h da manhã. Pais do aluno acionam a instituição na  justiça diante da omissão por parte da mesma."
    },
    {
      id: 2,
      cover: "https://noticias.memoria.araquari.ifc.edu.br/wp-content/uploads/sites/11/2016/12/IMG_0841-300x169.jpg",
      title: "Mochila roubada no IFC",
      date: "04/04/2025",
      font: "www.araquarinews.com.br",
      address: "http://localhost:5173",
      subject: "Mochila roubada na biblioteca do IFC - Campus Araquari às 3h da manhã. Pais do aluno acionam a instituição na  justiça diante da omissão por parte da mesma."
    },
    {
      id: 3,
      cover: "https://noticias.memoria.araquari.ifc.edu.br/wp-content/uploads/sites/11/2016/12/IMG_0841-300x169.jpg",
      title: "Mochila roubada no IFC",
      date: "05/04/2025",
      font: "www.araquarinews.com.br",
      address: "http://localhost:5173",
      subject: "Mochila roubada na biblioteca do IFC - Campus Araquari às 4h da manhã. Pais do aluno acionam a instituição na  justiça diante da omissão por parte da mesma."
    },
    {
      id: 4,
      cover: "https://noticias.memoria.araquari.ifc.edu.br/wp-content/uploads/sites/11/2016/12/IMG_0841-300x169.jpg",
      title: "Mochila roubada no IFC",
      date: "06/04/2025",
      font: "www.araquarinews.com.br",
      address: "http://localhost:5173",
      subject: "Mochila roubada na biblioteca do IFC - Campus Araquari às 5h da manhã. Pais do aluno acionam a instituição na  justiça diante da omissão por parte da mesma."
    },
    {
      id: 5,
      cover: "https://noticias.memoria.araquari.ifc.edu.br/wp-content/uploads/sites/11/2016/12/IMG_0841-300x169.jpg",
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
  <article class="news">
    <ul>
      <li v-for="(news, id) in newsletter" :key="id">
        <h2>{{ news.title }} | {{ news.date }}</h2>
        <img :src="news.cover" alt="Capa da noticia">
        <p>{{ news.subject }}</p>
        <div>
          <p>Fonte: <a :href="news.address">{{ news.address }}</a></p>
          <p>Link para o mesmo: {{ news.address }}</p>
        </div>
      </li>
    </ul>
  </article>
</template>
<style scoped>
  ul {
    /*display: flex;*/
    list-style: none;
    text-align: center;
  }
  /*img {
    
  }*/
</style>