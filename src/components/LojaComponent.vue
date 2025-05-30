<script setup>
defineProps(['adicionarCarrinho', 'listaLivros'])
</script>
<template>
    <section class="loja">
         <h2>Livros Disponíveis:</h2>
        <ul>
          <li v-for="livro in listaLivros" :key="livro.id">
            <img :src="livro.capa" alt="capa">
            <h3>{{ livro.nome }}</h3>
            <p>{{ livro.autor }}
              <span class="fa-regular fa-heart"></span>
            </p>
            <p>{{ livro.preco }}</p>
            <button
          v-if="!livro.adicionado"
          @click="$emit('adicionarCarrinho', livro)"
        >
          <span class="fa-solid fa-cart-shopping"></span>
        </button>
        <button v-else>Adicionado</button>
          </li>
        </ul>
      </section>
</template>
<style scoped>
.loja ul {
  display: flex;
  flex-wrap: wrap;
  margin: 0 3vw 0 7.5vw ;
  justify-content: center;
  padding: 0;
}
.loja ul li {
  margin: 6vw 1.5vw 3vw 1.5vw;
  width: 320px;
  margin: 2vw;
}
.loja h3 {
  font-family: "Patua One", serif;
  margin: 20px 0 0 0 ;
  font-size: 1rem;
}
.loja p {
  font-size: 1.1rem;
  margin: 10px 0 10px 0;
}
.loja button {
  font-size: 1.2rem;
  padding: 10px 100px 10px 100px;
  color: #FF5722;
  background-color: white;
  border: 2px solid #FF5722;
  margin: 10px 0 0 0;
  margin: 1vw 0 0 3px;
}
.loja h2 {
  font-size: 1.8rem;
  margin: 5vw 6vw 3vw 6vw;
  border-bottom: 2px solid #FF5722;
  width: 14%;
  padding: 0 0 10px 0;
}
</style>