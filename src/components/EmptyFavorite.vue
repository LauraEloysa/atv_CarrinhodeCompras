<script setup>
defineEmits('voltar')
</script>

<template>
    <section class="favoritosVazio">
        <p>Você ainda não tem favoritos</p>
        <font-awesome-icon :icon="['fas', 'heart-crack']" style="color: #2e649e; font-size: 2.3rem;" />
        <p><button @click="$emit('voltar')"> Volta para loja</button></p>
      </section>
</template>

<style scoped>

section.favoritosVazio {
  background-color: #4a88cb39;
  text-align: center;
  margin: 5vw;
  padding: 10vw;
  border-radius: 20px;
}

section.favoritosVazio p {
  font-size: 2rem;
  color: #4F4C57;
  font-weight: 700;
  margin-bottom: 1.5vw;
  margin-top: 1vw;
}

section.favoritosVazio button {
  background-color: #4a88cb;
  border: none;
  color: white;
  padding: 7px 30px;
  font-size: 1.04rem;
}

</style>