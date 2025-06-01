<script setup>
import { toRefs } from 'vue'
import SearchInput from '@/components/SearchInput.vue'

const props = defineProps({
  inputValue: String,
  listaCarrinho: Array,
  favoritos: Array
})

const emit = defineEmits(['update:inputValue', 'cart', 'favorite'])

function updateInputValue(value) {
  emit('update:inputValue', value)
}
</script>

<template>
  <header>
    <div>
      <ul class="logo">
        <li><a href="App.vue" style="color: black;">MundoLiterário</a></li>
        <li class="borderBlueEndColor">Apreço a <br> leitura</li>
      </ul>

      <ul>
        <li>
            <SearchInput :modelValue="inputValue" @update:modelValue="updateInputValue" />
          <FontAwesomeIcon class="iconePesquisa" icon="magnifying-glass" />
        </li>
      </ul>

      <ul class="menus">
        <li><a href="#">Termos</a></li>
        <li><a href="#">Equipe</a></li>
        <li><a href="#">Envio</a></li>
        <li><a href="#">Devolução</a></li>
      </ul>

      <ul class="Icones">
        <li class="carrinho" style="display: flex; align-items: center;">
          <FontAwesomeIcon icon="cart-shopping" @click="$emit('cart')" style="margin-right: 10px; cursor: pointer;" />
          <p>{{ listaCarrinho.length }}</p>
        </li>
        <li style="display: flex; align-items: center;">
          <FontAwesomeIcon icon="heart" @click="$emit('favorite')" style="margin-right: 10px; cursor: pointer;" />
          <p>{{ favoritos.length }}</p>
        </li>
        <li><FontAwesomeIcon icon="user" /></li>
      </ul>
    </div>
  </header>
</template>
