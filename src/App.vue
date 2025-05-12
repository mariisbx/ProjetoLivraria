<script setup>

 import { ref } from "vue";

let listaLivros = ref([
    {id: 1, nome: 'O livro de receitas dos Animes', autor: 'Nadine Estero', preco: 'R$119,90', sinapse: ' Este livro traz 75 receitas inspiradas nos pratos mais icônicos de diversos animes, como One Piece, My Hero Academia, Food Wars! e Dragon Ball Z. Cada receita é acompanhada de uma ilustração no estilo anime, além de informações sobre o episódio em que o prato aparece. Ideal para fãs de culinária e cultura japonesa.', capa: '/images/anime.webp' },
    {id: 2, nome: 'A Fisiologia do Gosto', autor: 'Jean Anthelme Brillat-Savarin', preco: 'R$89,90', sinapse: 'A Fisiologia do Gosto é uma reflexão profunda sobre a arte da gastronomia e os prazeres do paladar. Brillat-Savarin analisa como os sentidos, especialmente o gosto, influenciam as escolhas alimentares e como a culinária se conecta ao prazer e à cultura. O autor explora, com humor e sabedoria, o papel da comida na sociedade e no bem-estar humano. A obra é considerada uma das bases da gastronomia moderna e é indispensável para quem estuda ou aprecia a culinária.', capa: '/images/fisiologiadogosto.jpg' },
    {id: 3, nome: 'Harry Potter: O Livro de Receitas Oficial', autor: 'Joanna Farrow', preco: 'R$119,00', sinapse: ' Este livro traz mais de 40 receitas inspiradas nos filmes de Harry Potter, incluindo pratos doces e salgados, lanches, refeições, sobremesas e bebidas dignas de um banquete de Hogwarts. Entre as receitas, destacam-se os crepes de correio-coruja, o ensopado de Hagrid, os blondies de Draco Malfoy e a delícia melequenta do trasgo. Além disso, o livro oferece informações nutricionais e opções adaptadas para dietas vegetarianas, veganas e sem glúten.', capa: '/images/harrypotter.jpg'},
    {id: 4, nome: 'Le Cordon Bleu - Todas as técnicas culinárias', autor: 'Le Cordon Bleu', preco: 'R$199,00', sinapse: ' Este livro é uma obra abrangente que reúne mais de 200 receitas e técnicas essenciais da renomada escola de culinária Le Cordon Bleu. Organizado em capítulos que cobrem desde técnicas básicas até preparações mais avançadas, ele serve tanto para iniciantes quanto para profissionais que desejam aprimorar suas habilidades culinárias. Cada técnica é acompanhada de ilustrações detalhadas, facilitando a compreensão e execução das receitas.', capa: '/images/lecordonbleu.jpg'},
    {id: 5, nome: 'Manual de receitas da Magali', autor: 'Maurício de Sousa', preco: 'R$64,90', sinapse: ' Este livro é uma coletânea de receitas simples e deliciosas, inspiradas na personagem Magali da Turma da Mônica. Com ilustrações coloridas e instruções fáceis de seguir, é ideal para crianças e iniciantes na cozinha.', capa: '/images/magali.jpg' },
    {id: 6, nome: 'O Livro de Receitas do Menino Maluquinho', autor: 'Ziraldo', preco: 'R$24,90', sinapse: 'Neste livro, o Menino Maluquinho convida crianças e adultos a explorarem o mundo da culinária de forma divertida e educativa. Com 47 receitas testadas por uma equipe de crianças entre 8 e 11 anos, o livro oferece pratos simples e saborosos, ideais para serem preparados em família. As receitas incluem desde lanches rápidos até sobremesas criativas, todas ilustradas com o charme característico de Ziraldo e Mig. É uma excelente maneira de incentivar as crianças a se interessarem pela cozinha e desenvolverem habilidades culinárias desde cedo.', capa: '/images/maluquinho.jpg'},
    {id: 7, nome: 'Minhas receitas', autor: 'Patricia Lau', preco: 'R$29,90', sinapse: 'Esse livro vai te ajudar a preparar diversos pratos lindos e especiais para sua família e amigos. Inclui todo o passo a passo para preparação de comidas deliciosas para compor seus encontros familiares.', capa: '/images/minhareceita.jpeg'},
    {id: 8, nome: 'Pão Nosso', autor: 'Luiz Américo Camargo', preco: 'R$139,90', sinapse: 'Em Pão Nosso, Luiz Américo Camargo compartilha seu conhecimento sobre panificação artesanal, focando no uso do levain (fermento natural). O livro apresenta uma variedade de receitas, incluindo pães integrais, de nozes, de azeitona, de mandioca, baguetes e até panetone. Além disso, Camargo propõe pratos complementares como salada panzanella, rabanada salgada e ragu de linguiça, todos preparados com o pão caseiro como base. Com uma abordagem prática e acessível, o autor busca ensinar aos leitores como assar pães de qualidade superior aos encontrados em padarias tradicionais.', capa: '/images/paonosso.jpg'},
    {id: 9, nome: 'Les Recettes de Rémy – Ratatouille', autor: 'Nicole Seeman', preco: 'R$134,90', sinapse: 'Este livro é inspirado no filme Ratatouille, apresentando receitas do ratinho chef Remy. Inclui pratos como ratatouille, croquetes de peixe e sobremesas francesas clássicas. Perfeito para fãs da animação e da culinária francesa.', capa: '/images/ratatouille.jpg'},
    {id: 10, nome: 'Panelinha – Receitas que Funcionam', autor: 'Rita Lobo', preco: 'R$189,90', sinapse: 'Em Panelinha – Receitas que Funcionam, Rita Lobo reúne mais de 550 receitas práticas e saborosas, com foco em ingredientes acessíveis e sem ultraprocessados. O livro é dividido em categorias como jantares rápidos, saladas, massas, pratos com carnes, peixes e aves, além de sobremesas e pães integrais. Cada receita é acompanhada de dicas para facilitar o preparo e adaptar os pratos ao dia a dia. A obra também inclui orientações sobre utensílios de cozinha e grupos alimentares, promovendo uma alimentação saudável e consciente.', capa: '/images/receitasquefuncionam.webp'},
    {id: 11, nome: 'Joy of Cooking', autor: 'Irma S. Rombauer', preco: 'R$119,00', sinapse: 'Joy of Cooking é um dos livros de culinária mais vendidos dos Estados Unidos, com mais de 20 milhões de cópias vendidas desde sua publicação inicial. A obra é conhecida por seu estilo acessível e abrangente, tornando-se uma referência essencial para cozinheiros domésticos. Ela passou por diversas edições, adaptando-se às mudanças culturais e tecnológicas ao longo dos anos, mas sempre mantendo o espírito original de Irma.', capa: '/images/joyofcooking.jpg'},
    {id: 12, nome: 'Chef Brasil: Saboreando Histórias', autor: 'Dílvia Ludvichak', preco: 'R$42,90', sinapse: 'O livro narra a história do Chef Brasil, um personagem que viajou pelo mundo compartilhando suas experiências gastronômicas. A obra destaca a diversidade da culinária brasileira, influenciada por diversas culturas, como indígena, africana, portuguesa, árabe, chinesa e japonesa. Além disso, apresenta curiosidades sobre alimentos, ditos populares relacionados à comida e um calendário com as principais festas gastronômicas do Brasil, como a Festa do Pinhão em Santa Catarina.', capa: '/images/chefbrasil.jpeg'}
  ]);


    function sorteando() {
    const sorteio = Math.floor(Math.random() * listaLivros.value.length);
    return listaLivros.value[sorteio];
  }

  let livroSelecionado = ref(sorteando());

   let carrinho = ref([]);
  function adicionarCarrinho(livro) {
  const existente = carrinho.value.find(item => item.id === livro.id);

  if (existente) {
    existente.quantidade++;
  } else {
    livro.adicionado = true;
    livro.quantidade = 1;
    carrinho.value.push(livro);
  }
}

 const carrinhoVisivel = ref(false);
  const lojaVisivel = ref(true);

  function mostrarCarrinho() {
  carrinhoVisivel.value = true;
  lojaVisivel.value = false;
}

  function mostrarLoja() {
  carrinhoVisivel.value = false;
  lojaVisivel.value = true;
}

  function incrementar(item){
    item.quantidade++;
  }
  function decrementar(item){
    if (item.quantidade > 1) {
    item.quantidade--;
  }
}

  function removerItem(item) {
    const lixeira = carrinho.value.findIndex(livro => livro.id === item.id);
    if (lixeira !== -1) {
      carrinho.value.splice(lixeira, 1);
      item.adicionado = false;
      item.quantidade = 0;
      }
    }
</script>

<template>
    <div v-if="!carrinhoVisivel">
    <body>
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
        <li>
           <span @click="mostrarCarrinho" class="fa-solid fa-cart-shopping"></span>
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
    <main>
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
      <section  v-if="lojaVisivel" class="loja">
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
          @click="adicionarCarrinho(livro)"
        >
          <span class="fa-solid fa-cart-shopping"></span>
        </button>
        <button v-else>Adicionado</button>
          </li>
        </ul>
      </section>
    </main>
    <footer>
        <div>
     <h3>Saiba mais sobre nós:</h3>
      <ul>
        <li class="footerborda">
          <a href="App.vue"><span class="fa-brands fa-instagram"></span></a>
        </li>
        <li>
          <a href="App.vue"><span class="fa-brands fa-youtube"></span></a>
        </li>
      </ul>
    </div>
    <div>
     <h3>Tire dúvidas aqui:</h3>
     <input type="text">
    </div>
    <div>
      <p>Desenvolvido por: Maria Aparecida dos Santos Costa</p>
      <p>Alguns direitos reservados &copy; 2025</p>
    </div>
    </footer>
    </body>
    </div>
  <div v-else>
    <section class="carrinho" v-if="carrinho.length > 0">
      <h2>Seu Carrinho</h2>
      <div class="divcarrinho">
      <div>
      <ul v-for="item in carrinho" :key="item.id">
        <li>
          <p>
          <img :src="item.capa" alt="livro" id="capaCarrinho">
          </p>
        </li>
          <li id="espaco" >
            {{ item.nome }} - R${{ (parseFloat(item.preco.replace('R$', '').replace(',', '.')) * item.quantidade).toFixed(2) }}
          </li>
          <li id="espaco">
            <button @click="incrementar(item)">+</button>
          </li>
          <li id="espaco">
             {{ item.quantidade}}
          </li>
         <li id="espaco">
          <button @click="decrementar(item)">-</button>
         </li>
          <li id="espaco">
  <button @click="removerItem(item)"><span class="fa-solid fa-trash"></span></button>
          </li>
      </ul>
    </div>
    <div class="finalcompra">
     <h3 class="bordapreco">Total</h3>
     <div class="separarP">
      <p>Quantidade de itens:</p>
      <p class="bordamargin">{{ carrinho.reduce((total, item) => total + item.quantidade, 0)}}</p>
     </div>
     <div class="separarFrete">
     <p>Frete:</p>
     <p class="bordaespaco">Grátis</p>
    </div>
      <p class="pagamento"> Pagamento: R$ {{ carrinho.reduce((soma, item) => {
        const preco = parseFloat(item.preco.replace('R$', '').replace(',', '.'));
        return soma + (preco * item.quantidade);
      }, 0).toFixed(2) }}</p>
    </div>
  </div>
      <button class="voltarloja" @click="mostrarLoja">Voltar à loja</button>
    </section>
    <section class="carrinhovazio" v-else>
      <span class="fa-solid fa-cart-plus"></span>
      <p>Seu carrinho está vazio</p>
      <p>Clique aqui para adicionar itens:</p>
      <button @click="mostrarLoja">Loja</button>
    </section>
    </div>
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
.exibicao div.central {
  display: flex;
  padding: 8vw;
  margin: 2vw 0 0 8vw;
}
.exibicao div.texto {
  margin: 3vw 10vw 0 0;
}
img {
  width: 300px;
  height: 400px;
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
.carrinho div.divcarrinho {
  display: flex;
}
.carrinho img#capaCarrinho{
  width: 230px;
  height: 300px;
  margin: 0 28px 0 0;
}
.carrinho h2{
  margin: 3vw 3vw 0 3vw;
  font-size: 2rem;
  font-weight: 700;
  border-bottom: 2px solid #FF5722 ;
  width: 11%;
  padding: 0 0 8px 0;
}
.carrinho ul {
  display: flex;
  align-items: center;
  border-bottom: #FF5722 solid 2px;
  margin: 0 0 0 3vw;
  padding: 0 0 30px 0;
}
.carrinho ul li {
  margin: 4vw 1.2vw 2vw 5vw;
}
.carrinho ul li#espaco {
  margin: 2vw 10px 0 0 ;
  font-size: 1.3rem;
}
.carrinho li#espaco button {
  font-size: 1.4rem;
  padding: 4px 8px;
  background-color: white;
  border: none;
  border-radius: 5px;
  color: #7B7881;
}
.carrinho div.finalcompra {
  margin: 6vw 0 0 17vw;
  border: 2px solid #FF5722;
  padding: 3vw 3vw 0 3vw;
  height: 14vw;
}
.carrinho div.separarP {
  display: flex ;
  border-bottom: 2px solid #FF5722;
  padding: 0 0 14px 0;
}
.carrinho div.separarFrete {
  display: flex;
  border-bottom: 2px solid #FF5722;
  padding: 0 0 14px 0;
}
.carrinho h3{
  font-size: 1.6rem
}
.carrinho p{
  font-size: 1.2rem;
  margin: 1vw 0 0 0;
}
.carrinho div.finalcompra p.bordapreco{
  border-bottom: 2px solid #FF5722;
  padding: 0 0 14px 0;
}
.carrinho div.finalcompra p.bordamargin {
  margin: 19px 0 0 30px;
}
.carrinho div.finalcompra h3.bordapreco {
  border-bottom: 2px solid #FF5722;
  padding: 0 0 14px 0;
}
.carrinho div.finalcompra p.bordaespaco {
  margin: 19px 0 0 130px;
}
.carrinho p.pagamento {
  text-align: center;
}
.carrinho button.voltarloja {
  font-size: 1.2rem;
  padding: 6px;
  margin: 2vw 5vw;
  background-color: white;
  border: 2px solid #FF5722;
  border-radius: 10px;
}
.carrinhovazio {
  text-align: center;
  margin: 17vw 0 0 0;
}
.carrinhovazio span {
  color: #FF5722;
  font-size: 5rem;
}
.carrinhovazio p {
  font-size: 1.6rem;
  margin: 10px;
}
.carrinhovazio button {
  font-size: 1.4rem;
  padding: 6px;
  color: #FF5722;
  border: 2px solid #FF5722;
  border-radius: 5px;
  margin: 10px;
}
footer {
  margin: 2vw 2vw 3vw 8vw;
  display: flex;
  justify-content: space-between;
  background-color: #f1cf66;
  margin: 0;
  padding: 3vw;
  border-top: #FF5722 solid 2px;
}
footer p {
  line-height: 140%;
}
footer h3 {
  font-size: 1.3rem;
  margin: 0 0 0 14px;
}
footer a {
  color: #FF5722;
  font-size: 1.4rem;
}
footer input {
  padding: 0.4vw 0 0.4vw 1vw;
  font-size: 0.9rem;
  background-color: #F1f1f1;
  border: #FF5722 solid 2px;
  margin-right: 2vw;
  border-radius: 3px;
  margin: 1.5vw 0 0 0;
  border-radius: 12px;
}
footer ul {
  display: flex;
}
footer ul li {
  margin: 12px 0 0 45px;
}
footer ul li.footerborda {
  border-right: #FF5722 solid 2px;
  padding: 0 3vw 0 0;
}
</style>
