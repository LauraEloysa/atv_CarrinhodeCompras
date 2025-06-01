<script setup>
defineProps(['listaLivros', 'favoritos'])
defineEmits('voltar')
</script>

<template>
    <section class="favoritos">
        <h2> <span class="fa-solid fa-heart"></span> Meus Favoritos</h2>
        <ul>
          <li v-for="livro in listaLivros.filter(l => favoritos.includes(l.id))" :key="livro.id">
            <img :src="livro.capa" alt="Capa" width="80" />
            <p class="titulo">{{ livro.titulo }}</p>
            <p class="autor">{{ livro.autor }}</p>
            <p class="preco">R$ {{ livro.preco }}</p>
          </li>
        </ul>
        <button @click="$emit('voltar')">Voltar para loja</button>
      </section>
</template>

<style scoped>

section.favoritos {
  margin: 3vw 12vw;
}

section.favoritos ul {
  display: flex;
  flex-wrap: wrap;
  gap: 1.5rem;
  justify-content: center;
}

section.favoritos ul li {
  text-align: left;
  width: 19%;
  margin-right: 2.4vw;

}

section.favoritos h2 {
  color: #4a88cb;
  font-size: 2rem;
  font-weight: 600;
  margin-left: 2.4vw;
  margin-bottom: 2vw;
}

section.favoritos span {
  margin-right: 0.5vw;
}

section.favoritos ul li img {
  flex: 1 1 400px;
  width: 250px;
  height: 350px;
  margin-right: 2vw;
}

section.favoritos .titulo {
  font-size: 1.05rem;
  font-weight: 600;
  margin: 7px 0;
  line-height: 120%;
}

section.favoritos .autor {
  font-size: 0.9rem;
  color: #4F4C57;
  margin-bottom: 7px;
}

section.favoritos .preco {
  font-size: 1.02rem;
}
section.favoritos button {
  background-color: #4a88cb;
  color: white;
  margin-left: 2.4vw;
  margin-top: 2vw;
  font-size: 1.1rem;
  border: none;
  padding: 7px 20px;
}

</style>