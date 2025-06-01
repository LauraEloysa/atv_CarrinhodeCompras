<script setup>
const props = defineProps({
  livros: Array,
  listaCarrinho: Array,
  favoritos: Array
})

const emit = defineEmits(['adicionar-carrinho', 'adicionar-favoritos'])
</script>

<template>
  <div class="principal-pesquisa">
    <section class="pesquisa">
      <ul>
        <li v-for="livro in livros" :key="livro.id" class="livro-item">
          <img :src="livro.capa" alt="Capa do livro" width="200" height="280" />
          <h3>{{ livro.titulo }}</h3>
          <p>{{ livro.autor }}</p>
          <p>R$ {{ livro.preco }}</p>
          <div>
            <button
              @click="$emit('adicionar-carrinho', livro)"
              :class="listaCarrinho.some(item => item.id === livro.id) ? 'btn-adicionado' : 'btn-comprar'"
            >
              <FontAwesomeIcon icon="cart-shopping" />
              {{ listaCarrinho.some(item => item.id === livro.id) ? 'Adicionado' : 'Comprar' }}
            </button>

            <FontAwesomeIcon
              :icon="[favoritos.includes(livro.id) ? 'fas' : 'far', 'heart']"
              @click="$emit('adicionar-favoritos', livro.id)"
              style="cursor: pointer; margin-left: 1rem; color: #2e649e; font-size: 1.02rem;"
            />
          </div>
        </li>
      </ul>
    </section>
  </div>
</template>

<style scoped>
div.principal-pesquisa {
  margin: auto;
}

section.pesquisa {
  margin: 2vw 5vw 0 8vw;
}

section.pesquisa ul {
  display: flex;
  flex-wrap: wrap;
  text-align: left;  
}

section.pesquisa ul li {
  align-items: center;
  width: 19%;
  margin-bottom: 2vw;  
   display: grid;
}
section.pesquisa h3{
  width: 90%;
  color: #4F4C57;
  font-weight: 600;
}
section.pesquisa button{
background-color: #4a88cb;
color: white;
border: none;
padding: 5px 40px;
margin: 1vw 0 1vw 0;
}
section.pesquisa button:hover {
  transform: scale(1.02);
  transition: all 0.5s ease;
  background-color: #70a1d6;
}

section.pesquisa button.btn-adicionado {
  background-color: #28a745;
  padding: 5px 30px;
}
</style>