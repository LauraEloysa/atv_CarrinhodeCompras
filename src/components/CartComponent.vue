<script setup>
defineProps(['listaCarrinho']);
const emit = defineEmits('íncrementar-book', 'decrementar-book', 'lixeira', 'voltar')
</script>
<template>
    <section class="carrinho">
          <h2>
            <FontAwesomeIcon icon="truck" /> Seu Carrinho
          </h2>
          <ul>

            <li v-for="(book, index) in listaCarrinho" :key="index" style="display: flex; align-items: center;">
              <img :src="book.capa" alt="Capa do livro" width="100px" height="150px"
                style="margin-bottom: 1vw; margin-top: 1vw; " />
              <div style="display: flex; align-items: center; margin-left: 2vw; width: 30%;">
                <div>
                  <div>
                    <p class="titulo">{{ book.titulo }}</p>
                  </div>
                  <div>
                    <p class="autor">{{ book.autor }}</p>
                  </div>
                  <div>
                    <p class="preco"> R$ {{ book.preco }}</p>
                  </div>

                </div>
                <div class="lado" style="display: flex; width: 20%;">
                  <div style="display: flex; align-items: center;">
                     <div class="button" style="display: flex; align-items: center;">
                    <p @click="$emit('íncrementar-book', index)" style="cursor: pointer;">
                      +
                    </p>
                    <p style="margin: 0 10px;">
                      {{ book.contador }}
                    </p>
                    <p @click="$emit('decrementar-book', index)" style="cursor: pointer;">
                      -
                    </p>
                  </div>
                  <div>
                    <button class="lixeira" @click="$emit('lixeira', index)">
                      <span class="fa-solid fa-trash-can"></span>
                    </button>
                  </div>
                  </div>
                  <div>
                    <p>R${{ (book.preco * book.contador).toFixed(2) }}</p>
                  </div>
                </div>
              </div>
            </li>
          </ul>
          <button class="paginaPrincipal" @click="$emit('voltar')">
            Voltar para loja
          </button>
        </section>
  
</template>
<style scoped>

section.carrinho li {
  width: 90%;
  border-bottom: #4a88cb solid 2px;
  margin-right: 2vw;
}

section.carrinho .titulo {
  font-size: 1.4rem;
  font-weight: 600;
  line-height: 120%;
}

section.carrinho .autor {
  color: #4F4C57;
  margin-top: 0.4vw;
  margin-bottom: 0.4vw;
}

section.carrinho .preco {
  font-size: 1.1rem;
  color: #4F4C57;
  font-weight: 600;
}
section.carrinho .lado{
  align-items: center;
}
section.carrinho .button {
  padding: 3px 20px;
  border: 2px solid #4F4C57;
  margin: 0 0.5vw 0 3vw ;
  font-size: 1.01rem;
  font-weight: 600;
}
section.carrinho .lixeira{
  border: none;
  background-color: white;
  font-size: 1.2rem;
  margin-right: 5vw;
  font-weight: 500;
}
section.carrinho .lixeira:hover{
  color: #4a88cb;
  transition: 0.5s;
  scale: 1.1;
}
section.carrinho .lado {
  width: 10%;
  min-width: 60px;
  text-align: left;
}

section.carrinho h2 {
  font-size: 2rem;
  font-weight: 600;
  color: #4a88cb;
  margin: 2vw 0 2vw 3vw;
}

section.carrinho button.paginaPrincipal {
  background-color: #4a88cb;
  color: white;
  border: none;
  padding: 5px 15px;
  font-size: 1.03rem;
  margin: 2vw 0 2vw 2.5vw;
}

</style>