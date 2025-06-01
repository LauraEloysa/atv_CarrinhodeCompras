<script setup>
defineProps(['resumoLivro', 'favoritos', 'listaCarrinho'])
const emit = defineEmits(['voltar', 'adicionar-carrinho', 'adicionar-favorito'])
</script>
<template>
    <section>
        <div v-for="livro in resumoLivro" :key="livro.id" class="informacoes">
          <div>
            <img :src="livro.capa" alt="#" style="width: 490px; height: 570px; object-fit: contain;">
          </div>
          <div class="resumo">
            <h2>{{ livro.titulo }}</h2>
            <p style="color: #4F4C57; font-size: 1.1rem;">{{ livro.autor }}</p>
            <p class="resenha" style="font-size: 1.1rem;">{{ livro.resenha }}</p>
            <div style="align-items: center;">
              <button @click="$emit('adicionar-carrinho', livro)"
                :class="listaCarrinho.some(item => item.id === livro.id) ? 'btn-adicionado' : 'btn-comprar'"
                style="cursor: pointer;">
                <FontAwesomeIcon icon="cart-shopping" />
                {{listaCarrinho.some(item => item.id === livro.id) ? 'Adicionado' : 'Comprar'}}
              </button>

              <FontAwesomeIcon :icon="[favoritos.includes(livro.id) ? 'fas' : 'far', 'heart']"
                @click="$emit('adicionar-favorito', livro.id)"
                style="cursor: pointer; color: #2e649e; margin-left: 4rem; font-size: 1.4rem;" />
            </div>


          </div>
        </div>
        <button @click="$emit('voltar')" class="voltar">Voltar</button>
      </section>
</template>

<style scoped>
section.aba-livro .informacoes {
  display: flex;
  justify-content: space-between;
  margin: 3vw 8vw;
  border: #4a88cb 2px solid;
  padding: 2vw;
  align-items: center;
  border-radius: 5px;
}

section.aba-livro .informacoes .resumo {
  margin-left: 5vw;

}

section.aba-livro .informacoes h2 {
  font-size: 2rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
}

section.aba-livro .informacoes .resenha {
  margin-top: 4.5vw;
  margin-bottom: 6vw;
}

section.aba-livro .informacoes button {
  background-color: #4a88cb;
  color: white;
  border: none;
  padding: 0.5vw 7vw;
  font-size: 1.05rem;
  border-radius: 4px;
}

section.aba-livro .informacoes button:hover {
  transform: scale(1.01);
  transition: all 0.5s ease;
  background-color: #70a1d6;
}

section.aba-livro .informacoes button.btn-adicionado {
  background-color: #28a745;
  padding: 0.5vw 5.5vw;
}

section.aba-livro .voltar {
  margin-left: 8vw;
  background-color: #4a88cb;
  color: white;
  border: none;
  padding: 5px 60px;
  font-size: 1.1rem;
}
</style>