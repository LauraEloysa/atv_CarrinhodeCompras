<script setup>

import { ref } from 'vue'

const inputValue = ref('')

defineProps(['listaCarrinho']);
const emit = defineEmits(['limpar'])

const enviarCupom = () => {
  emit('limpar', inputValue.value)
  inputValue.value = '' 
}
</script>
<template>
          <section class="valorTotal">
          <div class="principal">
            <h2 style="font-weight: 600;">Total da compra:</h2>
            <div>
              <p class="espacoMaior">Produtos</p>
              <p> R$ {{listaCarrinho.reduce((soma, book) => soma + book.preco * book.contador, 0).toFixed(2)}}</p>
            </div>
            <div>
              <p class="espacoMaior">Frete</p>
              <p>Grátis</p>
            </div>
            <div class="semBorder">
              <p class="espacoMaior">Total</p>
              <p> R$ {{listaCarrinho.reduce((soma, book) => soma + book.preco * book.contador, 0).toFixed(2)}}</p>
            </div>
            <div class="semBorder">
              <button class="pagamento">Ir para pagamento</button>
            </div>
          </div>
          <input type="text" v-model="inputValue" placeholder="Código do cupon">
          <button class="button" @click="enviarCupom">Inserir cupom</button>
        </section>

</template>
<style scoped>
section.valorTotal {
  margin: auto;
}

section.valorTotal div.principal {
  border: #4F4C57 solid 2px;
  border-radius: 5px;
  padding: 2vw;
}

section.valorTotal div.principal div {
  display: flex;
  justify-content: space-between;
  border-bottom: #4a88cb solid 2px;
  margin-top: 2vw;
  margin-bottom: 0.5vw;
}

section.valorTotal .espacoMaior {
  margin-right: 10vw;
}

section.valorTotal .semBorder {
  border: none;
}

section.valorTotal input {
  margin: 1.5vw 1vw 0 0;
  background-color: #dce8f5;
  border: none;
  padding: 7px 40px 7px 15px;
  border-radius: 5px;
}

section.valorTotal .pagamento {
  background-color: #4a88cb;
  border: none;
  color: white;
  padding: 7px 90px;
}

section.valorTotal .button {
  background-color: #4a88cb;
  color: white;
  border: none;
  padding: 7px 20px;
  border-radius: 5px;
}

</style>