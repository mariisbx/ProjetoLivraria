<script setup>
defineEmits(['click-carrinho'])
</script>
<template>
    <header>
      <ul class="principal">
        <ul class="logo">
        <li>
          <a href="index.html">IFbooks</a>
        </li>
        <li class="p">Apreço a <br> leitura</li>
      </ul>
      <ul class="input-wrapper">
        <li>
          <input type="text" placeholder="Pesquisar">
          <span id="icone" class="fa-solid fa-magnifying-glass"></span>
        </li>
      </ul>
      <ul class="itens">
        <li>
          <a href="#">Termos</a>
        </li>
        <li>
          <a href="#">Equipe</a>
        </li>
        <li>
          <a href="#">Envio</a>
        </li>
        <li>
          <a href="#">Devoluções</a>
        </li>
       </ul>
        <ul class="icones">
        <li @click="$emit('click-carrinho')">
           <span class="fa-solid fa-cart-shopping"></span>
          </li>
        <li>
          <span id="borda" class="fa-solid fa-heart"></span>
        </li>
        <li>
          <span class="fa-solid fa-user"></span>
        </li>
      </ul>
      </ul>
    </header>
</template>
<style scoped>
header {
  margin: 0 0 5vw 0 ;
  background-color: #f1cf66;
  margin: 0 0 2vw 0;
  padding: 2vw 2vw 5vw 2vw;
  border-bottom: 2px solid #FF5722;
}
header ul.principal{
  display: flex;
  margin: 1.5vw 0 0 0;
}
header a {
  color:  black ;
}
header a:hover{
  color: #FF69B4;
}
header ul.logo {
  margin: 1.8vw 1vw 0 5vw;
  display: flex;
  color: #FF5722;
}

ul.logo li.p {
  font-size: 0.8rem;
  margin: 0 0 0 8px;
  border-left:2px solid #FF5722;
  padding: 0 0 0 7px;
}
ul.input-wrapper{
  margin: 1.5vw 0 0 5vw;
}
header ul li input {
  padding: 0.4vw 10vw 0.4vw 1vw;
  font-size: 0.9rem;
  background-color: #F1f1f1;
  border: solid 2px #FF5722;
  position: relative;
  margin-right: 2vw;
  border-radius: 5px;
}
header #icone {
  position: absolute;
  margin-left: 2vw;
  bottom: 45.9vw;
  left: 37.7vw;
  color: rgb(165, 163, 163);
}
header ul.itens{
  display: flex;
  margin: 1.8vw 0 0 2vw;
}
header ul.itens li {
  margin: 0 3vw;
}
header ul.icones {
  margin: 1.8vw 0 0 0;
  display: flex;
  color: black;
}
header ul.icones li span {
  margin: 0 0 0 2vw;
}
header ul.icones #borda {
  border-left: 2px solid  #FF5722;
  border-right: 2px solid #FF5722;
  padding: 0 1.8vw 0 1.8vw;
}
</style>