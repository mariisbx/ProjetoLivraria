<script setup>
defineProps(['livroSelecionado'])
</script>
<template>
    <section class="exibicao">
      <div class="central">
        <div class="texto">
          <p class="abril">Livro de Abril</p>
          <h1 class="nome">{{ livroSelecionado.nome }}</h1>
          <p class="autor">{{ livroSelecionado.autor }}</p>
          <p class="sinapse">{{ livroSelecionado.sinapse }}</p>
        </div>
        <div><img class="banner" :src="livroSelecionado.capa" alt="foto"></div>
      </div>
      </section>
</template>
<style scoped>
.exibicao div.central {
  display: flex;
  padding: 8vw;
  margin: 2vw 0 0 8vw;
}
.exibicao div.texto {
  margin: 3vw 10vw 0 0;
}

.exibicao {
  border-bottom: 2px solid #FF5722;
}
.exibicao div.texto p.abril {
  margin: 0 0 2vw 0;
  font-size: 1vw;
  border: 2px solid #FF5722;
  padding: 0.7vw;
  font-weight: 600;
  width: 70px;
  text-align: center;
  line-height: 120%;
  border-radius: 45px;
}
.exibicao div.texto h1.nome{
  font-family: "Patua One", serif;
  font-size: 2.5rem;
}
.exibicao div.texto p.autor {
  font-size: 1.3rem;
  margin: 30px 0 30px 0;
}
.exibicao div.texto p.sinapse {
  font-size: 1.2rem;
}
</style>