<script setup>

import { faHeart, fas } from '@fortawesome/free-solid-svg-icons'
import { ref } from 'vue'
const inputValue = ref('')

function limparInput() {
  inputValue.value = ''
}
const telaAtual = ref('loja');

const listaLivros = ref(
  [
    {
      id: 1,
      titulo: 'O Príncipe Cruel',
      resumo: 'O Príncipe Cruel, de Holly Black, é um romance de fantasia que acompanha uma garota humana vivendo entre fadas perigosas, onde precisa lutar por respeito e poder. A trama explora intrigas políticas, jogos de poder e amadurecimento em um mundo mágico e traiçoeiro.',
      resenha: 'Jude tinha apenas sete anos quando seus pais foram assassinados e ela, junto com suas irmãs, foi levada para viver na perigosa e encantadora Corte das Fadas. Apesar de ser humana, Jude deseja desesperadamente pertencer àquele mundo — mesmo sabendo que os feéricos desprezam mortais como ela. Entre eles, o príncipe Cardan se destaca por sua beleza cruel e por tornar a vida de Jude ainda mais difícil. No entanto, ela não se intimida. Determinada a conquistar seu lugar, Jude se envolve em intrigas políticas, jogos de poder e traições, mergulhando cada vez mais fundo no lado sombrio da corte. À medida que aprende a jogar o jogo deles, percebe que ser implacável pode ser sua única chance de sobreviver.',
      preco: 47.92,
      capa: '/image/OPrincipeCruel.jpg',
      autor: 'Holly Black',
      contador: 1
    },
    {
      id: 2,
      titulo: 'O Rei Perverso',
      resumo: 'O Rei Perverso, de Holly Black, continua a história de Jude Duarte, agora poderosa na corte das fadas, enquanto ela manipula jogos políticos para manter o rei Cardan sob seu controle. No entanto, traições e segredos ameaçam sua posição e seu coração.',
      resenha: 'Depois dos eventos de O Príncipe Cruel, Jude se vê em uma posição delicada: agora, ela detém o controle sobre o trono de Elfhame, manipulando o recém-coroado rei Cardan nos bastidores. Mesmo com o poder nas mãos, sua posição é frágil, pois traições e conspirações cercam a corte feérica. Jude precisa manter o controle político ao mesmo tempo em que lida com sua relação complexa com Cardan — intensa, instável e cheia de ressentimentos. Em meio a jogos de manipulação, alianças perigosas e segredos reveladores, Jude descobre que governar pode ser ainda mais perigoso do que conquistar o trono. Neste segundo volume, Holly Black aprofunda a tensão e a intriga, mantendo o leitor preso à trama do início ao fim.',
      preco: 47.84,
      capa: 'public/image/OReiPerverso.jpg',
      autor: 'Holly Black',
      contador: 1
    },
    {
      id: 3,
      titulo: 'A Rainha do Nada',
      resumo: 'A Rainha do Nada, de Holly Black, conclui a trilogia com Jude retornando ao mundo das fadas após ser exilada, determinada a recuperar seu poder e proteger aqueles que ama. Enfrentando guerras, alianças instáveis e seu amor por Cardan, ela descobre sua verdadeira força.',
      resenha: 'Ele será a destruição da coroa e a ruína do trono. Jude aprendeu que conquistar poder é fácil, mas mantê-lo é outra história. Após abrir mão do controle sobre o Rei Cardan em troca de poder, ela se tornou a Grande Rainha de Elfhame — mas vive exilada no mundo mortal, impotente e cheia de ressentimento. Quando sua irmã gêmea, Taryn, se vê em perigo por causa de Locke, Jude vê uma chance de agir: decide voltar ao Reino das Fadas fingindo ser Taryn. Para isso, precisa encarar seus sentimentos conflitantes por Cardan, o rei que a traiu. Em Elfhame, tudo mudou. A guerra está prestes a começar, e inimigos se aproximam. Jude terá que enfrentar conspirações, perigos e seu próprio coração. Será capaz de recuperar a coroa e o amor de Cardan? Ou perderá tudo?',
      preco: 43.65,
      capa: 'public/image/ARainhadoNada.jpg',
      autor: 'Holly Black',
      contador: 1
    },
    {
      id: 4,
      titulo: 'O canto mais escuro da floresta',
      resumo: 'Em Fairfold, humanos e fadas convivem, mas há perigos escondidos nas florestas. Hazel e seu irmão sempre imaginaram proteger o misterioso garoto de chifres adormecido. Quando ele desperta, segredos sombrios vêm à tona, e Hazel precisa virar a heroína que fingia ser na infância.',
      resenha: 'Hazel e seu irmão, Ben, vivem em Fairfold, onde humanos e o Povo do Ar coexistem em uma paz frágil. Turistas visitam a cidade para ver o garoto de chifres adormecido em um caixão de vidro, sem perceber o perigo escondido nas florestas. Desde pequenos, Hazel e Ben imaginam que ele é um príncipe encantado, e que são seus cavaleiros protetores. Mas, com o tempo, Hazel abandona essas fantasias, certa de que ele jamais despertará. Até que, um dia, ele acorda — e tudo muda. Criaturas antigas se agitam, segredos vêm à tona, e Hazel se vê forçada a enfrentar perigos reais. Agora, ela precisa se tornar a heroína que um dia fingiu ser. Em meio a magia, pactos sombrios e traições, Hazel e Ben descobrem que as histórias que contavam na infância podem ter sido mais reais do que imaginavam — e que talvez a coragem de antes seja a única esperança de sobrevivência.',
      preco: 35.15,
      capa: 'public/image/OCantoMaisEscuro.jpg',
      autor: 'Holly Black',
      contador: 1
    },
    {
      id: 5,
      titulo: 'Os dois morrem no final',
      resumo: '"Os Dois Morrem no Final" é um romance tocante que mostra como um único dia pode transformar tudo. Dois jovens desconhecidos se encontram para viver suas últimas 24 horas de forma inesquecível. Uma história sobre conexão, coragem e aproveitar cada segundo.',
      resenha: 'Imagine receber uma ligação informando que você vai morrer nas próximas 24 horas. É isso que acontece com Mateo e Rufus, dois jovens completamente diferentes, mas unidos pelo mesmo destino. Ambos são avisados pela Central da Morte que seu fim está próximo. Sem querer passar seu último dia sozinhos, eles se conectam por meio de um aplicativo chamado Último Amigo. Juntos, decidem viver intensamente suas últimas horas, explorando a cidade, compartilhando medos, sonhos e descobertas. Ao longo dessa jornada emocionante e cheia de humanidade, uma amizade inesperada se transforma em algo mais profundo. Uma história sobre como a vida pode ser bela mesmo diante do fim.',
      preco: 32.94,
      capa: 'public/image/OsDoisMorremNoFinal.jpg',
      autor: 'Adam Silveira',
      contador: 1
    },
    {
      id: 6,
      titulo: ' O primeiro a morrer no final',
      resumo: '"O Primeiro a Morrer no Final" é um emocionante prelúdio de "Os Dois Morrem no Final". Dois garotos se conhecem no dia em que a Central da Morte inicia seus alertas, e uma ligação pode mudar tudo. Uma narrativa intensa sobre destino, amor e o valor de viver o agora.',
      resenha: 'Na noite de 30 de julho de 2010, pessoas se reúnem em várias cidades dos EUA para a estreia da Central da Morte, um serviço que avisa se alguém vai morrer nas próximas 24 horas. Orion Pagan espera por isso há anos — convive com uma grave doença cardíaca e quer saber quando sua hora chegará para, enfim, viver sem medo. Já Valentino Prince, recém-chegado a Nova York, quer apenas começar sua nova vida e realizar seus sonhos. Quando os dois se conhecem sob as luzes da Times Square, surge uma conexão imediata. Mas, à meia-noite, uma ligação da Central muda tudo: um deles vai morrer em breve. Sem saber quem, como ou quando, eles decidem viver esse dia intensamente. Unidos pelo acaso e pelo tempo incerto, Orion e Valentino enfrentam o destino, com a única certeza de que querem estar juntos até o fim.',
      preco: 40.02,
      capa: 'public/image/OPrimeiroAMorrerNoFinal.jpg',
      autor: 'Adam Silveira',
      contador: 1
    },
    {
      id: 7,
      titulo: 'Os Sete Maridos de Evelyn Hugo',
      resumo: 'Uma lendária estrela de Hollywood decide revelar os segredos por trás de sua carreira e seus sete casamentos. Para isso, escolhe uma jornalista iniciante, surpreendendo a todos. O livro explora fama, amores proibidos e decisões que moldam uma vida.',
      resenha: 'Evelyn Hugo, lendária estrela de Hollywood, decide contar sua verdadeira história após décadas de fama, escândalos e segredos. Para isso, ela escolhe a jornalista iniciante Monique Grant, surpreendendo a todos. Conforme Evelyn revela detalhes íntimos de sua vida — incluindo os segredos por trás de seus sete casamentos —, Monique percebe que suas histórias estão mais entrelaçadas do que poderia imaginar. Entre glamour, amores proibidos e decisões difíceis, Evelyn narra sua luta por poder, identidade e amor em uma época que não permitia liberdade plena. Um romance poderoso sobre coragem, escolhas e o preço da fama, que nos faz repensar o que significa ser verdadeiro consigo mesmo.',
      preco: 33.91,
      capa: 'public/image/SeteMaridosDeEvelyn.jpg',
      autor: 'Taylor Jekkins Reid',
      contador: 1
    },
    {
      id: 8,
      titulo: 'De olho em você',
      resumo: 'Crystal Chen, influenciadora fora dos padrões do mundo fitness, encontra na academia seu refúgio após um término. Lá, cruza com Scott Ritchie, um bombeiro sarado e arrogante que desperta sua antipatia — e seu desejo. Entre disputas e provocações, os dois descobrem uma conexão inesperada. Para viver esse amor, Crystal terá que enfrentar preconceitos e reafirmar sua luta por autoestima e amor-próprio.',
      resenha: '"De Olho em Você" de Amy Lea é uma história encantadora que combina romance e autoestima. A protagonista, Crystal Chen, é uma influenciadora digital fora do padrão físico, que construiu sua carreira desafiando os estereótipos do mundo fitness. Após o fim de um namoro, ela encontra consolo na academia, onde sua vida vira de cabeça para baixo ao encontrar Scott Ritchie, um bombeiro sarado e arrogante. A rivalidade entre eles se intensifica, mas à medida que passam mais tempo juntos, descobrem que têm mais em comum do que imaginavam. Com temas de amor-próprio, superação de preconceitos e paixão inesperada, "De Olho em Você" é um romance envolvente e inspirador, perfeito para quem busca uma leitura leve, mas cheia de mensagens poderosas sobre autoestima e aceitação.',
      preco: 26.99,
      capa: 'public/image/DeOlhoEmVoce.jpg',
      autor: 'Amy Lea',
      contador: 1
    },
    {
      id: 9,
      titulo: 'Era uma vez um coração partido',
      resumo: 'Evangeline Raposa sempre acreditou em finais felizes, até ver o amor de sua vida prestes a se casar com outra. Desesperada, ela faz um perigoso acordo com Jacks, o sedutor e enigmático Príncipe de Copas: três beijos em troca de ajuda. Mas logo descobre que lidar com um imortal pode levá-la tanto ao seu conto de fadas quanto a uma tragédia inesquecível.',
      resenha: 'Era uma vez um coração partido é o primeiro livro da nova série de Stephanie Garber, autora da trilogia Caraval. A história acompanha Evangeline Fox, uma jovem que, ao descobrir que seu grande amor irá se casar com sua irmã postiça, faz um pacto com o enigmático Príncipe de Copas para impedir o casamento. Em troca, ele exige três beijos dela, a serem dados em momentos e locais escolhidos por ele. O livro mistura romance, magia e reviravoltas emocionantes, criando uma narrativa envolvente que explora temas como amor verdadeiro, sacrifício e os perigos de negociar com seres imortais. Ideal para fãs de fantasia e romances com toques de conto de fadas modernos.',
      preco: 45.55,
      capa: 'public/image/EraUmaVez.jpg',
      autor: 'Stephanie Garber',
      contador: 1
    },
    {
      id: 10,
      titulo: 'A balada do felizes para nunca',
      resumo: 'Após ser traída por Jacks, Evangeline Raposa decide nunca mais confiar nele. No entanto, ao descobrir uma nova maldição, ela é forçada a se unir novamente ao Príncipe de Copas. Com um feitiço mortal em jogo e novos inimigos surgindo, Evangeline precisa decidir se ainda pode seguir seu coração — ou se ele será sua ruína.',
      resenha: 'A aguardada sequência de Era Uma Vez Um Coração Partido traz uma nova aventura mágica e romântica. Após ser traída por Jacks, o Príncipe de Copas, Evangeline Raposa decide não mais confiar nele. Usando seus próprios poderes, ela acredita que pode reverter o destino e alcançar o tão sonhado final feliz. No entanto, uma nova e perigosa maldição a obriga a se aliar novamente a Jacks. Juntos, terão que enfrentar desafios ainda maiores, onde as regras do jogo mudam constantemente. Uma história repleta de magia, romance e escolhas difíceis, A Balada do Felizes para Nunca é uma leitura envolvente para quem adora um conto de fadas com reviravoltas e personagens cativantes. Não perca essa emocionante continuação!',
      preco: 42.48,
      capa: 'public/image/ABalada.jpg',
      autor: 'Stephanie Garber',
      contador: 1
    },
    {
      id: 11,
      titulo: 'A maldição do verdadeiro amor',
      resumo: 'Evangeline Raposa desperta sem memórias, casada com Apollo e vivendo em um castelo, mas sem saber o alto preço que pagou por esse conto de fadas. Enquanto seu marido esconde a verdade e planeja eliminar Jacks, o Príncipe de Copas, o amor verdadeiro será testado em meio a traições e segredos no desfecho da trilogia Era uma vez um coração partido.',
      resenha: 'A Maldição do Verdadeiro Amor é o emocionante desfecho da trilogia Era Uma Vez um Coração Partido, que conquistou leitores ao redor do mundo. A história acompanha Evangeline Raposa, que, após acordar sem memória, se vê casada com o príncipe Apollo em um castelo encantado. No entanto, ela desconhece o preço que pagou por esse "felizes para sempre". Determinados a manter seus segredos, Apollo e Jacks, o Príncipe de Copas, entram em uma batalha mortal, colocando à prova o verdadeiro significado do amor. Com reviravoltas surpreendentes e personagens cativantes, Garber entrega uma narrativa envolvente que mistura romance, magia e mistério. Ideal para fãs de fantasia e romances intensos.',
      preco: 48.28,
      capa: 'public/image/AMaldicao.jpg',
      autor: 'Stephanie Garber',
      contador: 1
    },
    {
      id: 12,
      titulo: 'Divinos Rivais',
      resumo: 'Iris Winnow, jovem jornalista, busca manter a família unida em meio a uma guerra entre deuses. Suas cartas ao irmão desaparecido vão parar nas mãos de Roman Kitt, seu rival, com quem cria uma ligação inesperada. Essa conexão a leva à linha de frente do conflito, em busca do irmão, da verdade e do amor.',
      resenha: 'Divinos Rivais é um romance da autora de sucesso, Stephanie Garber, que transporta os leitores para um mundo de magia, intriga e amores proibidos. A história segue os protagonistas enfrentando um universo de deuses e mitos, onde os destinos deles se entrelaçam de forma inesperada e apaixonante. No centro da trama, os personagens enfrentam dilemas sobre lealdade, poder e desejos conflitantes. Em um cenário onde os rivais são mais do que simples inimigos, mas figuras divinas com objetivos complexos, a narrativa é cheia de tensão, surpresas e momentos de pura magia. O livro é perfeito para quem ama uma mistura de romance, fantasia e drama com reviravoltas inesperadas. Uma leitura imperdível para fãs de histórias intensas e apaixonantes.',
      preco: 35.82,
      capa: 'public/image/DivinosRivais.jpg',
      autor: 'Rebecca Ross',
      contador: 1
    }
  ]
)
const favoriteBooks = ref([]);
const favoritos = ref([]);
function adicionarFavoritos(id) {
  const index = favoritos.value.indexOf(id)
  if (index === -1) {
    favoritos.value.push(id)
  } else {
    favoritos.value.splice(index, 1)
  }
}
function livroAleatorio() {
  const indice = Math.floor(Math.random() * listaLivros.value.length)
  return listaLivros.value[indice]
}
const livroEscolhido = ref(livroAleatorio());


const listaCarrinho = ref([]);

function adicionarCarrinho(book) {
  if (listaCarrinho.value.includes(book) == false) {
    listaCarrinho.value.push(book);
  }
}
function incrementar(index) {
  listaCarrinho.value[index].contador++
}

function decrementar(index) {

  const item = listaCarrinho.value[index]
  item.contador--
  if (item.contador <= 0) {
    listaCarrinho.value.splice(index, 1)
    return contador.value == 1;
  }
}
const resumoLivro = ref([]);

function abaLivros(livro) {
  resumoLivro.value = [livro];
  telaAtual.value = 'abaLivros'
}
</script>

<template>
  <main>
    <header>
      <div>

        <ul class="logo">
          <li>
            <a href="App.vue" style="color: black;">MundoLiterário</a>
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
          <li class="carrinho" style="display: flex; align-items: center;">
            <FontAwesomeIcon icon="cart-shopping" @click="telaAtual = 'carrinho'"
              style="margin-right: 10px; cursor: pointer;" />
            <p>{{ listaCarrinho.length }}</p>
          </li>
          <li style="display: flex; align-items: center;">
            <FontAwesomeIcon icon="heart" @click="telaAtual = 'favoritos'"
              style="margin-right: 10px; cursor: pointer;" />
            <p>{{ favoritos.length }}</p>
          </li>
          <li>
            <FontAwesomeIcon icon="user" />
          </li>
        </ul>

      </div>

    </header>

    <body>
      <div v-if="telaAtual === 'loja'">
        <section class="random" style="display: flex; align-items: center;">
          <div>
            <p class="autor">{{ livroEscolhido.autor }}</p>
            <p class="titulo"> {{ livroEscolhido.titulo }}</p>
            <p class="resumo">{{ livroEscolhido.resumo }}</p> <button>Acessar página do livro</button>
          </div>
          <div>
            <img :src="livroEscolhido.capa" alt="#"
              style="flex: 1 1 400px; width: 320px; height:450px; box-shadow: 3px 3px 5px #4F4C57; margin-left: 15vw;">

          </div>
        </section>
        <section class="informacoes">
          <div>
            <FontAwesomeIcon icon="truck" />
            <p>
              Frete grátis para SC
            </p>
          </div>
          <div style="border-left: #2e649e solid 2px; border-right: #2e649e solid 2px; margin: 0 6vw">
            <FontAwesomeIcon icon="star" style="margin-left: 5.5vw;" />
            <p style="margin-right: 5.5vw; ">
              Livros recomendados
            </p>
          </div>
          <div>
            <FontAwesomeIcon icon="book-open" />
            <p>
              Mais vendidos
            </p>
          </div>
        </section>
        <section class="livros">

          <ul style="display: flex; flex-wrap: wrap; gap: 1.5rem; justify-content: center;">

            <li v-for="livro in listaLivros" :key="livro.id" style="width: 19%; justify-items: left;">
              <img :src="livro.capa" alt="#" style="flex: 1 1 400px; width: 250px; height:350px;"
                @click="abaLivros(livro)">

              <p style="justify-items: left; white-space: pre-line; font-weight: 600;font-size: 1.1rem;">{{ livro.titulo
                }}</p>

              <p style="color: #4F4C57; font-weight: 400; font-size: 0.9rem; margin-top: 0.2vw;">{{ livro.autor }}</p>

              <div style="display: flex; align-items: center; font-size: 1.06rem; margin-bottom: 1vw;">

                <p style="margin-top:0.2vw ;">R${{ livro.preco }}</p>

                <FontAwesomeIcon :icon="[favoritos.includes(livro.id) ? 'fas' : 'far', 'heart']"
                  @click="adicionarFavoritos(livro.id)"
                  style="cursor: pointer; margin-left: 1rem; color: #2e649e; margin-left: 10.5rem;" />

              </div>
              <button @click="adicionarCarrinho(livro)"
                :class="listaCarrinho.some(item => item.id === livro.id) ? 'btn-adicionado' : 'btn-comprar'"
                style="cursor: pointer;">
                <FontAwesomeIcon icon="cart-shopping" />
                {{listaCarrinho.some(item => item.id === livro.id) ? 'Adicionado' : 'Comprar'}}
              </button>
            </li>
          </ul>
        </section>
      </div>

      <div v-if="listaCarrinho.length == 0 && telaAtual === 'carrinho'" class="carrinho-vazio">
        <p>
          <img src="https://cdn-icons-png.flaticon.com/512/11010/11010851.png" alt="Carrinho" width="120px">
        </p>
        <p style="font-size: 2.1rem; font-weight: 700; ">Seu carrinho está vazio</p>

        <p>
          <button @click="telaAtual = 'loja'">Voltar para a loja</button>
        </p>

      </div>

      <div v-if="telaAtual === 'carrinho' && listaCarrinho.length > 0" style="display: flex;">
        <section class="carrinho">
          <h2>
            <FontAwesomeIcon icon="truck" /> Seu Carrinho
          </h2>
          <ul>

            <li v-for="(book, index) in listaCarrinho" :key="index" style="display: flex; align-items: center;">
              <img :src="book.capa" alt="Capa do livro" width="100px" height="150px"
                style="margin-bottom: 1vw; margin-top: 1vw; " />
              <div style="display: flex; align-items: center; margin-left: 2vw; width: 30%;">
                <div>
                  <div>
                    <p class="titulo">{{ book.titulo }}</p>
                  </div>
                  <div>
                    <p class="autor">{{ book.autor }}</p>
                  </div>
                  <div>
                    <p class="preco"> R$ {{ book.preco }}</p>
                  </div>

                </div>
                <div class="lado" style="display: flex; width: 20%;">
                  <div class="button" style="display: flex;">
                    <p @click="incrementar(index)" style="cursor: pointer;">
                      +
                    </p>
                    <p style="margin: 0 10px;">
                      {{ book.contador }}
                    </p>
                    <p @click="decrementar(index)" style="cursor: pointer;">
                      -
                    </p>
                  </div>
                  <div>
                    <p>R${{ (book.preco * book.contador).toFixed(2) }}</p>
                  </div>
                </div>
              </div>
            </li>
          </ul>
          <button class="paginaPrincipal" @click="telaAtual = 'loja'">
            Voltar para loja
          </button>
        </section>
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
          <button class="button" @click="limparInput">Inserir cupom</button>
        </section>
        
      </div>
  <section v-if="telaAtual === 'abaLivros'" class="aba-livro">
    <div v-for="livro in resumoLivro" :key="livro.id" class="informacoes">
      <div>
        <img :src="livro.capa" alt="#" style="width: 490px; height: 570px; object-fit: contain;">
      </div>
      <div class="resumo">
        <h2>{{ livro.titulo }}</h2>
      <p style="color: #4F4C57; font-size: 1.1rem;">{{ livro.autor }}</p>
      <p class="resenha" style="font-size: 1.1rem;">{{ livro.resenha }}</p>
      <div style="align-items: center;">
        <button @click="adicionarCarrinho(livro)"
                :class="listaCarrinho.some(item => item.id === livro.id) ? 'btn-adicionado' : 'btn-comprar'"
                style="cursor: pointer;">
                <FontAwesomeIcon icon="cart-shopping" />
                {{listaCarrinho.some(item => item.id === livro.id) ? 'Adicionado' : 'Comprar'}}
              </button>
              
              <FontAwesomeIcon :icon="[favoritos.includes(livro.id) ? 'fas' : 'far', 'heart']"
                  @click="adicionarFavoritos(livro.id)"
                  style="cursor: pointer; color: #2e649e; margin-left: 4rem; font-size: 1.4rem;" />
      </div>
      

      </div>
      
      
    </div>
    <button @click="telaAtual = 'loja'"class="voltar">Voltar</button>
  </section>

      <section v-if="telaAtual === 'favoritos' && favoritos.length == 0" class="favoritosVazio">
        <p>Você ainda não tem favoritos</p>
        <font-awesome-icon :icon="['fas', 'heart-crack']" style="color: #2e649e; font-size: 2.3rem;" />
        <p><button @click="telaAtual = 'loja'"> Volta para loja</button></p>
      </section>
      <section v-if="telaAtual === 'favoritos' && favoritos.length > 0" class="favoritos">
        <h2> <span class="fa-solid fa-heart"></span> Meus Favoritos</h2>
        <ul>
          <li v-for="livro in listaLivros.filter(l => favoritos.includes(l.id))" :key="livro.id">
            <img :src="livro.capa" alt="Capa" width="80" />
            <p class="titulo">{{ livro.titulo }}</p>
            <p class="autor">{{ livro.autor }}</p>
            <p class="preco">R$ {{ livro.preco }}</p>
          </li>
        </ul>
        <button @click="telaAtual = 'loja'">Voltar para loja</button>
      </section>
    </body>
  </main>
  <footer>
    <div class="footer">
      <div class="redesSociais">
        <p>Mundo Literário</p>
        <ul style="display: flex;">
          <li><span class="fa-brands fa-square-facebook"></span></li>
          <li><span class="fa-brands fa-instagram"></span></li>
          <li><span class="fa-brands fa-square-twitter"></span></li>
        </ul>
      </div>
      <div class="contato">
        <p>Contato</p>
        <ul class="telefone">
          <li><font-awesome-icon icon="phone" />
            <p>+55 47 40045263</p>
          </li>
          <li><span class="fa-solid fa-clock"></span>
            <p>8h às 23h - Seg a Sex</p>
          </li>
          <li><span class="fa-solid fa-envelope"></span>
            <p>contato@mundoliterario.com</p>
          </li>
        </ul>
        <ul style="display: flex;" class="cartoes">
          <li><img src="/image/Paypal.png" alt=""></li>
          <li><img src="/image/Mastercard.png" alt=""></li>
          <li><img src="/image/VISA.png" alt=""></li>
        </ul>
      </div>
    </div>
    <div class="copy">
      <p>&copy; Alguns direitos reservados. Mundo Literário 2025. </p>
    </div>
  </footer>
</template>

<style scoped>
section.random {
  margin: 2vw 11.5vw;
}

section.random .autor {
  border: 2px solid #4a88cb;
  width: 25%;
  text-align: center;
  color: #4a88cb;
  font-size: 1.05rem;
}

section.random .titulo {
  font-size: 3rem;
  font-weight: 700;
  line-height: 100%;
  margin: 2vw 0;
}

section.random .resumo {
  width: 90%;

}

section.random button {
  margin-top: 2vw;
  background-color: #4a88cb;
  color: white;
  border: none;
  padding: 0.5vw 2vw;
  font-size: 1.1rem;
}

section.informacoes {
  display: flex;
  border-bottom: #4a88cb solid 2px;
  border-top: #4a88cb solid 2px;
  padding: 4vw 0;
  justify-content: center;
}

section.informacoes div {
  display: flex;
  font-size: 1.2rem;
  padding: 2vw;
  align-items: center;
}

section.informacoes div p {
  font-weight: 600;
  margin-left: 0.6vw;
}

section.livros ul li {
  line-height: 200%;
  margin-top: 2VW;
}

section.livros li img:hover {
  transform: scale(1.03);
  transition: all 0.5s ease;
}

section.livros button {
  background-color: #4a88cb;
  color: white;
  border: none;
  padding: 0.5vw 6vw;
  border-radius: 4px;
}

section.livros button:hover {
  transform: scale(1.01);
  transition: all 0.5s ease;
  background-color: #70a1d6;
}

section.livros button.btn-adicionado {
  background-color: #28a745;
  padding: 0.5vw 5.5vw;
}

div.carrinho-vazio {
  text-align: center;
  align-items: center;
  background-color: #70a1d63b;
  border-radius: 10px;
  margin: 5vw 2vw 0 2vw;
  padding: 10vw 0;
}

div.carrinho-vazio button {
  background-color: #4a88cb;
  border: none;
  font-size: 1.1rem;
  color: white;
  padding: 5px 20px;
  border-radius: 5px;
  margin-top: 1vw;
}

section.carrinho li {
  width: 90%;
  border-bottom: #4a88cb solid 2px;
  margin-right: 2vw;
}

section.carrinho .titulo {
  font-size: 1.4rem;
  font-weight: 600;
  line-height: 120%;
}

section.carrinho .autor {
  color: #4F4C57;
  margin-top: 0.4vw;
  margin-bottom: 0.4vw;
}

section.carrinho .preco {
  font-size: 1.1rem;
  color: #4F4C57;
  font-weight: 600;
}

section.carrinho .button {
  padding: 3px 20px;
  border: 2px solid #4F4C57;
  margin: 0 3vw;
  font-size: 1.01rem;
  font-weight: 600;
}

section.carrinho .lado {
  width: 10%;
  min-width: 60px;
  text-align: left;
}

section.carrinho h2 {
  font-size: 2rem;
  font-weight: 600;
  color: #4a88cb;
  margin: 2vw 0 2vw 3vw;
}

section.carrinho button.paginaPrincipal {
  background-color: #4a88cb;
  color: white;
  border: none;
  padding: 5px 15px;
  font-size: 1.03rem;
  margin: 2vw 0 2vw 2.5vw;
}

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

section.favoritos {
  margin: 3vw 12vw;
}

section.favoritos ul {
  display: flex;
  flex-wrap: wrap;
  gap: 1.5rem;
  justify-content: center;
}

section.favoritos ul li {
  text-align: left;
  width: 19%;
  margin-right: 2.4vw;

}

section.favoritos h2 {
  color: #4a88cb;
  font-size: 2rem;
  font-weight: 600;
  margin-left: 2.4vw;
  margin-bottom: 2vw;
}

section.favoritos span {
  margin-right: 0.5vw;
}

section.favoritos ul li img {
  flex: 1 1 400px;
  width: 250px;
  height: 350px;
  margin-right: 2vw;
}

section.favoritos .titulo {
  font-size: 1.05rem;
  font-weight: 600;
  margin: 7px 0;
  line-height: 120%;
}

section.favoritos .autor {
  font-size: 0.9rem;
  color: #4F4C57;
  margin-bottom: 7px;
}

section.favoritos .preco {
  font-size: 1.02rem;
}

section.favoritos button {
  background-color: #4a88cb;
  color: white;
  margin-left: 2.4vw;
  margin-top: 2vw;
  font-size: 1.2rem;
  border: none;
  padding: 7px 20px;
}

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

section.aba-livro .informacoes{
  display: flex;
  justify-content: space-between;
  margin: 3vw 8vw;    
  border: #4a88cb 2px solid;
  padding: 2vw;
  align-items: center;
  border-radius: 5px;
}
section.aba-livro .informacoes .resumo{
  margin-left: 5vw;

}

section.aba-livro .informacoes h2{
  font-size: 2rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
}
section.aba-livro .informacoes .resenha{
  margin-top: 4.5vw;
  margin-bottom: 6vw;
}
section.aba-livro .informacoes button {
  background-color: #4a88cb;
  color: white;
  border: none;
  padding: 0.5vw 7vw;
  font-size: 1.05rem;
  border-radius: 4px;
}
section.aba-livro .informacoes button:hover {
  transform: scale(1.01);
  transition: all 0.5s ease;
  background-color: #70a1d6;
}

section.aba-livro .informacoes button.btn-adicionado {
  background-color: #28a745;
  padding: 0.5vw 5.5vw;
}
section.aba-livro .voltar{
  margin-left: 8vw;
  background-color: #4a88cb;
  color: white;
  border: none;
  padding: 5px 60px;
  font-size: 1.1rem;
}
</style>