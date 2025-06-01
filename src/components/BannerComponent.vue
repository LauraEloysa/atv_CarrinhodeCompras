<script setup>
const emit = defineEmits('abrirLivro')
defineProps(['livroEscolhido'])
</script>
<template>
    <section class="random" style="display: flex; align-items: center;">
          <div>
            <p class="autor">{{ livroEscolhido.autor }}</p>
            <p class="titulo"> {{ livroEscolhido.titulo }}</p>
            <p class="resumo">{{ livroEscolhido.resumo }}</p>
            <button @click="$emit('abrirLivro', livroEscolhido)">Acessar página do livro</button>
          </div>
          <div>
            <img :src="livroEscolhido.capa" alt="#"
              style="flex: 1 1 400px; width: 320px; height:450px; box-shadow: 3px 3px 5px #4F4C57; margin-left: 15vw;">

          </div>
        </section>
</template>

<style scoped>
section.random {
  margin: 2vw 11.5vw;
}

section.random .autor {
  border: 2px solid #4a88cb;
  width: 30%;
  text-align: center;
  color: #4a88cb;
  font-size: 1.05rem;
}

section.random .titulo {
  font-size: 3rem;
  font-weight: 700;
  line-height: 100%;
  margin: 2vw 0;
}

section.random .resumo {
  width: 90%;

}

section.random button {
  margin-top: 2vw;
  background-color: #4a88cb;
  color: white;
  border: none;
  padding: 0.5vw 2vw;
  font-size: 1.1rem;
}

</style>