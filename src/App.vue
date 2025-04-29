
<script setup>
import { ref } from 'vue'
const inputValue = ref('')

function limparInput() {
  inputValue.value = ''
}
</script>
<template>
  <main>
    <header>
      <div>

        <ul class="logo">
          <li>
            MundoLiterário
          </li>
          <li class="borderBlueEndColor">
            Apreço a <br>
            leitura
          </li>
        </ul>

        <ul>
          <li>
            <input type="text" v-model="inputValue" placeholder="Pesquisar">
            <FontAwesomeIcon class="iconePesquisa" icon="magnifying-glass" @click="limparInput" />
          </li>
        </ul>

        <ul class="menus">
          <li><a href="#">Termos</a></li>
          <li><a href="#">Equipe</a></li>
          <li><a href="#">Envio</a></li>
          <li><a href="#">Devolução</a></li>
        </ul>

        <ul class="Icones">
          <li class="carrinho">
            <FontAwesomeIcon icon="cart-shopping" />
          </li>
          <li>
            <FontAwesomeIcon icon="heart" />
          </li>
          <li>
            <FontAwesomeIcon icon="user" />
          </li>
        </ul>

      </div>

    </header>
  </main>
</template>

<style scoped>

main a {
  text-decoration: none;
}
main ul li {
  list-style-type: none;
}

header{
  border-bottom: solid #4a88cb 1.5px ;
}
header div{
  display: flex;
  justify-content: space-between;
  margin: 1vw 5vw;
}
header ul{
  display: flex;
  align-items: center;
  width: 30%;
}
header .logo li{
  margin-right: 1vw;
}
header ul li.borderBlueEndColor{
  margin-right: 1vw;
  padding-left: 1vw;
  border-left: #4a88cb solid 2px;
  font-size: small;
  color: #4a88cb;
}
header input{
  border: none;
  background-color: #dce8f5;
  padding: 0.4vw 10vw  0.4vw 1vw;
  position: relative;
  margin-right: 2vw;
  border-radius: 3px;
}
header .iconePesquisa {
 position: absolute;
  margin-left: 2vw;
  bottom: 45.2vw;
  left: 44vw;
  color: #2e649e;
}
header .menus {
  margin-right: 3vw;

}
header .menus li a{
  margin-right: 3vw;
  color: #7B7881;
}
header .Icones{
  margin-left: -4vw;
}
header .Icones li{
  border-left: #4a88cb solid 2px;
  padding-left: 2vw;
  margin-right: 2vw;
  color: #4a88cb;
}
header .Icones li.carrinho{
  border: none;
}
</style>
