<script setup>
        defineEmits('voltar')
</script>
<template>
    <div class="carrinho-vazio">
        <p> 
          <img src="https://cdn-icons-png.flaticon.com/512/11010/11010851.png" alt="Carrinho" width="120px">
        </p>
        <p style="font-size: 2.1rem; font-weight: 700; ">Seu carrinho está vazio</p>

        <p>
          <button @click="$emit('voltar')">Voltar para a loja</button>
        </p>

    </div>

</template>

<style scoped>

.carrinho-vazio {
  text-align: center;
  align-items: center;
  background-color: #70a1d63b;
  border-radius: 10px;
  margin: 5vw 2vw 0 2vw;
  padding: 10vw 0;
}

.carrinho-vazio button {
  background-color: #4a88cb;
  border: none;
  font-size: 1.1rem;
  color: white;
  padding: 5px 20px;
  border-radius: 5px;
  margin-top: 1vw;
}

</style>