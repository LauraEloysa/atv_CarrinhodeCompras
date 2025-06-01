<script setup>
    defineProps(['listaLivros', 'favoritos', 'listaCarrinho'])
    const emit = defineEmits('AdicionaCarrinho', 'AdicionarFavoritos', 'abrirLivros')
</script>

<template>
         <section class="livros">

          <ul style="display: flex; flex-wrap: wrap; gap: 1.5rem; justify-content: center;">

            <li v-for="livro in listaLivros" :key="livro.id" style="width: 19%; justify-items: left;">
              <img :src="livro.capa" alt="#" style="flex: 1 1 400px; width: 250px; height:350px;"
                @click="$emit('abrirLivros', livro)">

              <p style="justify-items: left; white-space: pre-line; font-weight: 600;font-size: 1.1rem;">{{ livro.titulo
              }}</p>

              <p style="color: #4F4C57; font-weight: 400; font-size: 0.9rem; margin-top: 0.2vw;">{{ livro.autor }}</p>

              <div style="display: flex; align-items: center; font-size: 1.06rem; margin-bottom: 1vw;">

                <p style="margin-top:0.2vw ;">R${{ livro.preco }}</p>

                <FontAwesomeIcon :icon="[favoritos.includes(livro.id) ? 'fas' : 'far', 'heart']"
                  @click="$emit('AdicionarFavoritos', livro.id)"
                  style="cursor: pointer; margin-left: 1rem; color: #2e649e; margin-left: 10.5rem;" />

              </div>
              <button @click="$emit('AdicionarCarrinho', livro)"
                :class="listaCarrinho.some(item => item.id === livro.id) ? 'btn-adicionado' : 'btn-comprar'"
                style="cursor: pointer;">
                <FontAwesomeIcon icon="cart-shopping" />
                {{listaCarrinho.some(item => item.id === livro.id) ? 'Adicionado' : 'Comprar'}}
              </button>
            </li>
          </ul>
        </section>
</template>

<style scoped>

section.livros ul li {
  line-height: 200%;
  margin-top: 2VW;
}

section.livros li img:hover {
  transform: scale(1.03);
  transition: all 0.5s ease;
}

section.livros button {
  background-color: #4a88cb;
  color: white;
  border: none;
  padding: 0.5vw 6vw;
  border-radius: 4px;
}

section.livros button:hover {
  transform: scale(1.01);
  transition: all 0.5s ease;
  background-color: #70a1d6;
}

section.livros button.btn-adicionado {
  background-color: #28a745;
  padding: 0.5vw 5.5vw;
}

</style>