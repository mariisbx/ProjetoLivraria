<template>
    <section class="categorias">  
      <ul>
          <li class="border">
            <span id="truck" class="fa-solid fa-truck-fast"></span>
            <p>Frete Grátis para o litoral</p>
          </li>
          <li>
            <span id="star" class="fa-solid fa-star"></span>
            <p>Mais vendidos</p>
          </li>
          <li class="borderb">
            <span id="livros" class="fa-solid fa-book-open"></span>
            <p>Livros recomendados</p>
          </li>
        </ul>
      </section>
</template>
<style scoped>
.categorias {
  margin: 4vw 0 0 0;
  border-bottom: 2px solid #FF5722;
  padding: 0 0 5vw 0;
}
.categorias ul {
  display: flex;
}
.categorias ul li {
  margin: 2vw 8vw 2vw 5vw;
}
.categorias ul span#star {
  margin: 0 10px 8px 52px;
}
.categorias ul span#truck {
  margin: 0 10px 8px 106px;
}
.categorias ul span#livros {
  margin: 0 10px 8px 83px;
}
.categorias ul span {
  font-size: 2rem;
  color: #FF5722;
}
.categorias ul li p {
  font-size: 1.3rem;
  width: 130%;
  font-weight: 700;
}
.categorias ul li.border {
  border-right: #FF5722 solid 3px;
  padding: 0 7vw;
}
.categorias ul li.borderb {
  border-left: #FF5722 solid 3px;
  padding: 0 7vw;
}
</style>