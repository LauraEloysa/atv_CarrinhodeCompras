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
      resenha: 'Primeiro livro da mais nova série de Holly Black. Conheça a impressionante história de uma garota mortal que se vê presa em uma teia de intrigas reais. Jude tinha 7 anos quando seus pais foram assassinados e foi forçada a viver no Reino das Fadas. Dez anos depois, tudo o que ela quer é ser como eles – lindos e imortais – e realmente pertencer ao Reino das Fadas, apesar de sua mortalidade. Mas muitos do povo das Fadas desprezam os humanos. Especialmente o Príncipe Cardan, o filho mais jovem, mais bonito e mais cruel do Grande Rei. Para ganhar um lugar na Alta Corte, ela deve desafiá-lo... e enfrentar as consequências. Envolvida em intrigas e traições do palácio, Jude descobre sua própria capacidade para truques e derramamento de sangue. Mas, com a ameaça de uma guerra civil e o Reino das Fadas por um fio, Jude precisará arriscar sua vida em uma perigosa aliança para salvar suas irmãs, e o próprio Reino. Com personagens únicos, reviravoltas inesperadas, e uma traição de tirar o fôlego, este livro vai deixar o leitor pedindo bis – querendo mergulhar de cabeça na continuação deste universo.',
      preco: 47.92,
      capa: '/image/OPrincipeCruel.jpg',
      autor: 'Holly Black',
      contador: 1
    },
    {
      id: 2,
      titulo: 'O Rei Perverso',
      resumo: 'O Rei Perverso, de Holly Black, continua a história de Jude Duarte, agora poderosa na corte das fadas, enquanto ela manipula jogos políticos para manter o rei Cardan sob seu controle. No entanto, traições e segredos ameaçam sua posição e seu coração.',
      resenha: 'Para sobreviver no Reino das Fadas, Jude Duarte precisou aprender muitas lições. A mais importante delas veio de seu padrasto: o poder é bem mais fácil de adquirir do que de manter. Ela achou que, depois de enganar Cardan para que ele jurasse obedecê-la por um ano e um dia, sua vida se tornaria mais fácil. Mas ter qualquer influência sobre o Grande Rei de Elfhame parece uma tarefa impossível, principalmente quando ele faz de tudo em seu poder para humilhá-la e prejudicá-la, mesmo que seu fascínio pela garota humana permaneça intacto. Agora, com as ondas ameaçando engolir a terra e um alerta de traição iminente, Jude precisa lutar para salvar a própria vida e a daqueles que ama, além de lutar contra seus sentimentos conflituosos por Cardan no meio-tempo. Em um mundo imortal, um ano e um dia não são nada...',
      preco: 47.84,
      capa: 'public/image/OReiPerverso.jpg',
      autor: 'Holly Black',
      contador: 1
    },
    {
      id: 3,
      titulo: 'A Rainha do Nada',
      resumo: 'A Rainha do Nada, de Holly Black, conclui a trilogia com Jude retornando ao mundo das fadas após ser exilada, determinada a recuperar seu poder e proteger aqueles que ama. Enfrentando guerras, alianças instáveis e seu amor por Cardan, ela descobre sua verdadeira força.',
      resenha: 'Ele será a destruição da coroa e a ruína do trono.O poder é mais fácil de adquirir do que de manter. Jude aprendeu a lição mais difícil de sua vida quando abdicou do controle do Rei Cardan em troca de um poder imensurável.Agora, ela carrega o outrora impensável título de Grande Rainha de Elfhame, mas as condições são longe de ser ideais. Exilada por Cardan no mundo mortal, Jude se encontra impotente e frustrada enquanto planeja reivindicar tudo que Cardan tomou dela.A oportunidade surge com sua irmã gêmea, cuja vida está em perigo. Para salvá-la de uma situação tenebrosa envolvendo Locke, Jude decide voltar ao Reino das Fadas se passando por Taryn. Antes disso, porém, ela precisa confrontar os próprios sentimentos contraditórios pelo rei que a traiu.No entanto, ao voltar a Elfhame, Jude constata que tudo mudou. A guerra está prestes a eclodir, e ela caminha próximo a seus inimigos. Será que ela vai ser capaz de resgatar a Coroa e o amor incondicional de Cardan, ao mesmo tempo que destrói os planos de seus inimigos? Ou será que tudo está perdido para sempre?',
      preco: 43.65,
      capa: 'public/image/ARainhadoNada.jpg',
      autor: 'Holly Black',
      contador: 1
    },
    {
      id: 4,
      titulo: 'O canto mais escuro da floresta',
      resumo: 'Em Fairfold, humanos e fadas convivem, mas há perigos escondidos nas florestas. Hazel e seu irmão sempre imaginaram proteger o misterioso garoto de chifres adormecido. Quando ele desperta, segredos sombrios vêm à tona, e Hazel precisa virar a heroína que fingia ser na infância.',
      resenha: 'Hazel e seu irmão, Ben, moram em Fairfold, uma cidade onde humanos e o Povo do Ar convivem pacificamente. Turistas visitam o lugar para testemunhar as maravilhas do Povo e o elemento mais maravilhoso ali, o garoto de chifres. Mas os visitantes nunca conseguem ver o perigo daquelas árvores.Desde crianças, Hazel e Ben criam histórias sobre o garoto no caixão de vidro. Que ele é um príncipe e os dois são cavaleiros em sua guarda. Fingem e esperam, de todo o coração, que seu príncipe seja diferente das outras fadas, que fazem acordos cruéis, escondem-se nas sombras das árvores e amaldiçoam turistas...Mas, à medida que cresce, Hazel vai deixando as histórias de lado. Ela sabe que o garoto de chifres nunca irá acordar.E então, um dia... ele acorda.E tudo vira de cabeça para baixo. Hazel precisa se tornar o cavaleiro que um dia fingiu ser. Numa história de amor puro, lealdades que não se revelam e a pontada ferina da traição, a garota e seu irmão se perguntam se a coragem dos tempos de infância será suficiente para salvá-los.',
      preco: 35.15,
      capa: 'public/image/OCantoMaisEscuro.jpg',
      autor: 'Holly Black',
      contador: 1
    },
    {
      id: 5,
      titulo: 'Os dois morrem no final',
      resumo: '"Os Dois Morrem no Final" é um romance tocante que mostra como um único dia pode transformar tudo. Dois jovens desconhecidos se encontram para viver suas últimas 24 horas de forma inesquecível. Uma história sobre conexão, coragem e aproveitar cada segundo.',
      resenha: 'No dia 5 de setembro, pouco depois da meia-noite, Mateo Torrez e Rufus Emeterio recebem uma ligação da Central da Morte. A notícia é devastadora: eles vão morrerquele mesmo dia.Os dois não se conhecem, mas, por motivos diferentes, estão à procura de um amigo com quem compartilhar os últimos momentos, uma conexão verdadeira que ajude a diminuir um pouco a angústia e a solidão que sentem. Por sorte, existe um aplicativo para isso, e é graças a ele que Rufus e Mateo vão se encontrar para uma última grande aventura: viver uma vida inteira em um único dia.Uma história sensível e emocionante, Os dois morrem no final nos lembra o que significa estar vivo. Com seu olhar único, Adam Silvera mostra que cada segundo importa, e mesmo que não haja vida sem morte, nem amor sem perda, tudo pode mudar em 24 horas.',
      preco: 32.94,
      capa: 'public/image/OsDoisMorremNoFinal.jpg',
      autor: 'Adam Silveira',
      contador: 1
    },
    {
      id: 6,
      titulo: ' O primeiro a morrer no final',
      resumo: '"O Primeiro a Morrer no Final" é um emocionante prelúdio de "Os Dois Morrem no Final". Dois garotos se conhecem no dia em que a Central da Morte inicia seus alertas, e uma ligação pode mudar tudo. Uma narrativa intensa sobre destino, amor e o valor de viver o agora.',
      resenha: 'Na noite de 30 de julho de 2010, as pessoas se reúnem em diversas cidades dos Estados Unidos para a inauguração da Central da Morte, um serviço controverso capaz de informar se seus usuários terão um encontro prematuro com a morte ao longo das próximas 24 horas.Orion Pagan espera há anos que alguém lhe diga quando vai morrer. Só assim ele conseguirá aproveitar um pouco a vida, sem o temor de não saber quando a doença grave que tem no coração o fará partir dessa para a melhor.Receber uma ligação da Central da Morte é a última coisa que Valentino Prince deseja. Após deixar o Arizona e se mudar para Nova York, ele mal pode esperar para viver esse novo capítulo de sua história e realizar seus sonhos.Sob as luzes da Times Square, Orion e Valentino se conhecem, e a conexão entre eles é imediata. Mas, à meia-noite, a primeira ligação da Central da Morte anuncia que um dos dois vai morrer em breve. Embora não saibam como — ou quando — o dia vai terminar, eles só têm uma certeza: querem ficar juntos até o fim.',
      preco: 40.02,
      capa: 'public/image/OPrimeiroAMorrerNoFinal.jpg',
      autor: 'Adam Silveira',
      contador: 1
    },
    {
      id: 7,
      titulo: 'Os Sete Maridos de Evelyn Hugo',
      resumo: 'Uma lendária estrela de Hollywood decide revelar os segredos por trás de sua carreira e seus sete casamentos. Para isso, escolhe uma jornalista iniciante, surpreendendo a todos. O livro explora fama, amores proibidos e decisões que moldam uma vida.',
      resenha: 'Lendária estrela de Hollywood, Evelyn Hugo sempre esteve sob os holofotes ― seja estrelando uma produção vencedora do Oscar, protagonizando algum escândalo ou aparecendo com um novo marido… pela sétima vez. Agora, prestes a completar oitenta anos e reclusa em seu apartamento no Upper East Side, a famigerada atriz decide contar a própria história ― ou sua “verdadeira história” ―, mas com uma condição: que Monique Grant, jornalista iniciante e até então desconhecida, seja a entrevistadora. Ao embarcar nessa misteriosa empreitada, a jovem repórter começa a se dar conta de que nada é por acaso ― e que suas trajetórias podem estar profunda e irreversivelmente conectadas.',
      preco: 33.91,
      capa: 'public/image/SeteMaridosDeEvelyn.jpg',
      autor: 'Taylor Jekkins Reid',
      contador: 1
    },
    {
      id: 8,
      titulo: 'De olho em você',
      resumo: 'Crystal Chen, influenciadora fora dos padrões do mundo fitness, encontra na academia seu refúgio após um término. Lá, cruza com Scott Ritchie, um bombeiro sarado e arrogante que desperta sua antipatia — e seu desejo. Entre disputas e provocações, os dois descobrem uma conexão inesperada. Para viver esse amor, Crystal terá que enfrentar preconceitos e reafirmar sua luta por autoestima e amor-próprio.',
      resenha: 'Crystal Chen é uma influenciadora digital que tem o corpo fora do padrão e construiu a carreira lutando contra os estereótipos do mundo fitness. Após o fim do seu último namoro, ela está sem nenhuma paciência para os homens e seu único refúgio passa a ser a academia – seu templo de autoestima e positividade.Até que Scott Ritchie se matricula no mesmo lugar. Já no primeiro dia, o bombeiro sarado que exala arrogância – e gostosura – comete um pecado imperdoável: invade o aparelho preferido de Crystal antes que ela termine de usar e conquista sua antipatia imediata.Dia após dia, enquanto esses inimigos mortais e ultracompetitivos disputam o território da academia, as faíscas de desejo entre eles se multiplicam. Mesmo assim, a última coisa que eles esperam é se encontrar fora de seu campo de batalha diário e constatar que têm mais em comum do que achavam.Ao descobrir que dentro daquele peito musculoso bate um coração sensível, Crystal decide baixar a guarda. Mas antes de poder vivenciar plenamente essa paixão, ela precisa passar pelo teste de força mais importante de sua vida: enfrentar o preconceito e superar todos os obstáculos para continuar divulgando sua mensagem de amor-próprio.',
      preco: 26.99,
      capa: 'public/image/DeOlhoEmVoce.jpg',
      autor: 'Amy Lea',
      contador: 1
    },
    {
      id: 9,
      titulo: 'Era uma vez um coração partido',
      resumo: 'Evangeline Raposa sempre acreditou em finais felizes, até ver o amor de sua vida prestes a se casar com outra. Desesperada, ela faz um perigoso acordo com Jacks, o sedutor e enigmático Príncipe de Copas: três beijos em troca de ajuda. Mas logo descobre que lidar com um imortal pode levá-la tanto ao seu conto de fadas quanto a uma tragédia inesquecível.',
      resenha: 'Criada na loja de antiguidades de seu querido pai, cercada por lendas de seres poderosos e imortais, Evangeline Raposa cresceu acreditando em histórias de amores verdadeiros e em finais felizes. Mas essas crenças se veem abaladas quando a jovem descobre que o amor de sua vida está prestes a se casar com outra pessoa.Seu desespero é tamanho que ela aceita fazer um acordo com o harmoso e perverso Príncipe de Copas, famoso por seu poderio mítico. Dizem que seu beijo é tão encantador que vale a pena morrer por ele, e é justamente isso que o príncipe pede em troca: três beijos de Evangeline a serem dados no momento e no local escolhidos previamente.Logo, Evangeline descobre que negociar com um imortal é um jogo muito perigoso. Afinal, o Príncipe de Copas quer muito mais dela do que apenas beijos. Ele tem outros planos para a jovem, e tais intenções podem tanto se tornar o tão sonhado “felizes para sempre” quanto a mais requintada tragédia.',
      preco: 45.55,
      capa: 'public/image/EraUmaVez.jpg',
      autor: 'Stephanie Garber',
      contador: 1
    },
    {
      id: 10,
      titulo: 'A balada do felizes para nunca',
      resumo: 'Após ser traída por Jacks, Evangeline Raposa decide nunca mais confiar nele. No entanto, ao descobrir uma nova maldição, ela é forçada a se unir novamente ao Príncipe de Copas. Com um feitiço mortal em jogo e novos inimigos surgindo, Evangeline precisa decidir se ainda pode seguir seu coração — ou se ele será sua ruína.',
      resenha: 'Após ser traída por Jacks, o Príncipe de Copas, Evangeline Raposa jura nunca mais confiar nele. Depois de ter descoberto a própria magia, ela acredita que poderá usá-la para restaurar sua chance de um “felizes para sempre”.Mas, quando outra maldição terrível é revelada, Evangeline se vê obrigada a estar novamente ao lado do Príncipe de Copas. Só que, desta vez, novas regras serão impostas. Jacks não é a única pessoa com quem Evangeline precisa ter cuidado. Na verdade, apesar de sua vontade de desprezá-lo, talvez ele seja aquele em quem a jovem possa confiar de fato.Agora, em vez de um feitiço de amor causando estragos na vida de Evangeline, um feitiço assassino foi lançado. E para quebrá-lo, ela e Jacks terão que lutar contra novos inimigos e uma mágica que brinca com mentes e corações.Evangeline sempre seguiu seu coração, mas será que ela pode confiar nele desta vez?',
      preco: 42.48,
      capa: 'public/image/ABalada.jpg',
      autor: 'Stephanie Garber',
      contador: 1
    },
    {
      id: 11,
      titulo: 'A maldição do verdadeiro amor',
      resumo: 'Evangeline Raposa desperta sem memórias, casada com Apollo e vivendo em um castelo, mas sem saber o alto preço que pagou por esse conto de fadas. Enquanto seu marido esconde a verdade e planeja eliminar Jacks, o Príncipe de Copas, o amor verdadeiro será testado em meio a traições e segredos no desfecho da trilogia Era uma vez um coração partido.',
      resenha: 'Ao se aventurar pelo Magnifico Norte, Evangeline Raposa continuava em busca de seu final feliz. Após acordar sem se recordar do passado, ela se vê casada com Apollo e o lendário castelo do príncipe é, aparentemente, sua nova morada.Porém, para viver esse suposto conto de fadas, Evangeline precisou pagar um preço devastador sem nem ao menos fazer ideia disso. Ela desconhece tudo aquilo que perdeu, e se depender de seu marido… a jovem nunca descobrirá. Ele está tão determinado a garantir a ignorância de sua esposa que pretende dar um fim à vida de Jacks – o Príncipe de Copas.Com sangue sendo derramado e corações sendo usurpados, o verdadeiro amor vai ser colocado à prova no último livro da trilogia Era uma vez um coração partido. A maldição do verdadeiro amor é a aguardada conclusão desta história encantadora que arrebatou corações ao redor do mundo.',
      preco: 48.28,
      capa: 'public/image/AMaldicao.jpg',
      autor: 'Stephanie Garber',
      contador: 1
    },
    {
      id: 12,
      titulo: 'Divinos Rivais',
      resumo: 'Iris Winnow, jovem jornalista, busca manter a família unida em meio a uma guerra entre deuses. Suas cartas ao irmão desaparecido vão parar nas mãos de Roman Kitt, seu rival, com quem cria uma ligação inesperada. Essa conexão a leva à linha de frente do conflito, em busca do irmão, da verdade e do amor.',
      resenha: 'Após séculos adormecidos, os deuses estão em guerra novamente. No entanto, a única preocupação de Iris Winnow, uma jovem jornalista de dezoito anos, é manter sua família unida e em segurança.Enquanto a mãe de Iris sofre para superar um vício e o irmão está desaparecido em meio às trincheiras da guerra, a melhor forma de a garota atingir seu objetivo é conquistando a vaga de colunista no jornal onde trabalha, a Gazeta de Oath.Enquanto isso, para lidar com suas preocupações, Iris escreve cartas para o irmão. Porém, misteriosamente, elas vão parar nas mãos de Roman Kitt, seu insensível e fascinante rival na redação do jornal.Quando ele passa a responder anonimamente as cartas, os dois criam uma conexão mágica que seguirá Iris até a linha de frente da batalha, em uma busca por seu irmão, pela salvação da humanidade e pelo amor.',
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
          <li class="carrinho"  style="display: flex; align-items: center;">
            <FontAwesomeIcon icon="cart-shopping" @click="telaAtual = 'carrinho'" style="margin-right: 10px;"/>
            <p>{{ listaCarrinho.length }}</p>
          </li>
          <li style="display: flex; align-items: center;">
            <FontAwesomeIcon icon="heart"
            @click="telaAtual = 'favoritos'"  style="margin-right: 10px;"/>
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
              <img :src="livro.capa" alt="#" style="flex: 1 1 400px; width: 250px; height:350px; ">

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
                :class="listaCarrinho.some(item => item.id === livro.id) ? 'btn-adicionado' : 'btn-comprar'">
                <FontAwesomeIcon icon="cart-shopping" />
                {{listaCarrinho.some(item => item.id === livro.id) ? 'Adicionado' : 'Comprar'}}
              </button>
            </li>
          </ul>
        </section>
      </div>

      <div v-if="listaCarrinho.length == 0 && telaAtual === 'carrinho'"class="carrinho-vazio"> 
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
          <h2><FontAwesomeIcon icon="truck" /> Seu Carrinho </h2>
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
                    <p @click="incrementar(index)">
                      +
                    </p>
                    <p style="margin: 0 10px;">
                      {{ book.contador }}
                    </p>
                    <p @click="decrementar(index)">
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
            <p> R$ {{ listaCarrinho.reduce((soma, book)=> soma + book.preco * book.contador, 0).toFixed(2) }}</p>
          </div>
          <div>
            <p class="espacoMaior">Frete</p>
            <p>Grátis</p>
          </div>
          <div class="semBorder">
            <p class="espacoMaior">Total</p>
            <p> R$ {{ listaCarrinho.reduce((soma, book)=> soma + book.preco * book.contador, 0).toFixed(2) }}</p>
          </div>
          <div class="semBorder">
            <button class="pagamento">Ir para pagamento</button>
          </div>
          </div>
          <input type="text"  v-model="inputValue" placeholder="Código do cupon">
          <button class="button" @click="limparInput">Inserir cupom</button>
        </section>
      </div>
      <section v-if="favoritos.length == 0">
        <p>Você não tem favoritos</p>
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
        <p>+55 47 40045263</p></li>
        <li><span class="fa-solid fa-clock"></span>
        <p>8h às 23h - Seg a Sex</p></li>
        <li><span class="fa-solid fa-envelope"></span>
        <p>contato@mundoliterario.com</p></li>
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
div.carrinho-vazio{
  text-align: center;
  align-items: center;
  background-color: #70a1d63b;
  border-radius: 10px;
  margin: 5vw 2vw 0 2vw;
  padding: 10vw 0;
}
div.carrinho-vazio button{
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
section.carrinho h2{
  font-size: 2rem;
  font-weight: 600;
  color: #4a88cb;
  margin: 2vw 0 2vw 3vw;
}
section.carrinho button.paginaPrincipal{
  background-color: #4a88cb;
  color: white;
  border:  none;
  padding: 5px 15px;
  font-size: 1.03rem;
  margin: 2vw 0 2vw 2.5vw;
}
section.valorTotal{
  margin: auto;
}
section.valorTotal div.principal{
  border: #4F4C57 solid 2px;
  border-radius: 5px;
  padding: 2vw;
}
section.valorTotal div.principal div{
  display: flex;
  justify-content: space-between;
  border-bottom: #4a88cb solid 2px;
  margin-top: 2vw;
  margin-bottom: 0.5vw;
}
section.valorTotal .espacoMaior{
  margin-right: 10vw;
}
section.valorTotal .semBorder{
  border: none;
}
section.valorTotal input{
  margin: 1.5vw 1vw 0 0;
  background-color:  #dce8f5;
  border: none;
  padding: 7px 40px 7px 15px;
  border-radius: 5px;
}
section.valorTotal .pagamento{
  background-color: #4a88cb;
  border: none;
  color: white;
  padding: 7px 90px;
}
section.valorTotal .button{
  background-color: #4a88cb;
  color: white;
  border: none;
  padding: 7px 20px;
  border-radius: 5px;
}
section.favoritos{
  margin: 3vw 12vw ;
}
section.favoritos ul{
  display: flex;
  flex-wrap: wrap; gap: 1.5rem; justify-content: center;
}
section.favoritos ul li{
  text-align: left;
  width: 19%;
  margin-right: 2.4vw;
  
}
section.favoritos h2{
  color: #4a88cb;
  font-size: 2rem;
  font-weight: 600;
  margin-left: 2.4vw;
  margin-bottom: 2vw;
}
section.favoritos span{
  margin-right: 0.5vw;
}
section.favoritos ul li img{
  flex: 1 1 400px;
   width: 250px; 
  height:350px;
  margin-right: 2vw;
}
section.favoritos .titulo{
  font-size: 1.05rem;
  font-weight: 600;
  margin: 7px 0;
  line-height: 120%;
}
section.favoritos .autor{
  font-size: 0.9rem;
  color: #4F4C57;
  margin-bottom: 7px;
}
section.favoritos .preco{
  font-size: 1.02rem;
}
section.favoritos button{
  background-color: #4a88cb;
  color: white;
  margin-left: 2.4vw;
  margin-top: 2vw;
  font-size: 1.2rem;
  border: none;
  padding: 7px 20px;
}
</style>