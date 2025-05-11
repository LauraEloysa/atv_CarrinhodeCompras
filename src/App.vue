<script setup>

import { faHeart, fas } from '@fortawesome/free-solid-svg-icons'
import { computed, ref } from 'vue'
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
    },
    {
      id: 13,
      titulo: 'Promessas cruéis',
      resumo: 'Duas semanas após um coração partido, Iris retorna à linha de frente como correspondente de guerra para impedir novas tragédias. Enquanto isso, Roman acorda sem memória no reino de Dacre, escrevendo em favor do deus que o salvou. Uma carta misteriosa o faz questionar sua lealdade, encerrando a duologia com romance, magia e decisões difíceis.',
      resenha: 'Duas semanas se passaram desde que Iris Winnow voltou para casa com o coração partido. Mas a guerra está longe do fim, e a cidade de Oath segue mergulhada em ignorância e descrença. Determinada a impedir mais tragédias, Iris retorna à linha de frente como correspondente de guerra, buscando alertar outras cidades antes que o caos as alcance. Enquanto isso, Roman Kitt desperta no reino de Dacre sem memória, escrevendo artigos em apoio ao deus que o curou. No entanto, tudo muda quando uma carta misteriosa surge em seu guarda-roupa, forçando-o a escolher entre a lealdade a Dacre ou a verdade sobre si mesmo. Com romance, magia e escolhas impossíveis, Promessas Cruéis encerra a duologia Divinos Rivais com intensidade e emoção.',
      preco: 35.69,
      capa: 'public/image/PromessasCrueis.jpg',
      autor: 'Rebecca Ross',
      contador: 1
    },
      {
      id: 14,
      titulo: 'A rainha vermelha',
      resumo: 'Em um mundo dividido pelo sangue, Mare Barrow, uma vermelha sem esperanças, descobre um poder misterioso diante da elite prateada. Mesmo com sangue vermelho, ela desafia a ordem ao revelar habilidades sobrenaturais. Entre intrigas, príncipes e escolhas perigosas, Mare se vê no centro de uma revolução.',
      resenha: 'O mundo de Mare Barrow é dividido pelo sangue: vermelho ou prateado. Mare e sua família são vermelhos: plebeus, humildes, destinados a servir uma elite prateada cujos poderes sobrenaturais os tornam quase deuses. Mare rouba o que pode para ajudar sua família a sobreviver e não tem esperanças de escapar do vilarejo miserável onde mora. Entretanto, numa reviravolta do destino, ela consegue um emprego no palácio real, onde, em frente ao rei e a toda a nobreza, descobre que tem um poder misterioso… Mas como isso seria possível, se seu sangue é vermelho? Em meio às intrigas dos nobres prateados, as ações da garota vão desencadear uma dança violenta e fatal, que colocará príncipe contra príncipe - e Mare contra seu próprio coração.',
      preco: 32.72,
      capa: 'public/image/RainhaVermelha.jpg',
      autor: 'Victoria Aveyard',
      contador: 1
    },
    {
      id: 15,
      titulo: 'Espada de vidro',
      resumo: 'Mare Barrow, uma vermelha com poderes elétricos, torna-se alvo da coroa após revelar suas habilidades. Fugindo do controle real, ela busca outros como ela para formar um exército contra a opressão prateada. Com a guerra se aproximando, Mare enfrenta inimigos externos e o risco de perder a própria essência.',
      resenha: 'O sangue de Mare Barrow é vermelho como o da população comum, mas seu poder de controlar a eletricidade a torna tão letal quanto os prateados da elite. Após ter sua habilidade revelada em rede nacional, Mare se torna uma arma viva — algo que a coroa quer controlar a qualquer custo. Ao escapar do palácio, ela descobre que não está sozinha: existem outros vermelhos com dons como o seu. Em fuga, Mare parte em uma missão para encontrá-los e formar um exército capaz de enfrentar a tirania prateada. Mas enquanto a guerra se aproxima e as escolhas se tornam mais cruéis, ela precisará lutar não só contra seus inimigos — mas contra o perigo de se tornar o próprio mal que jurou destruir.',
      preco: 54.33,
      capa: 'public/image/EspadaVidro.jpg',
      autor: 'Victoria Aveyard',
      contador: 1
    },
      {
      id: 16,
      titulo: 'A prisão do rei',
      resumo: 'Prisioneira no palácio e sem poderes, Mare Barrow é usada como símbolo de controle por Maven, o rei que a traiu. Enquanto resiste ao cativeiro, a Guarda Escarlate cresce, preparando-se para a guerra. Cal, dividido entre o dever e o amor, precisa escolher seu caminho em meio ao caos iminente.',
      resenha: 'Mare Barrow está prisioneira no palácio, sem seus poderes, sufocada pelas Pedras Silenciosas e assombrada pelas consequências de suas escolhas. Refém de Maven, o rei cruel que um dia amou — e que a traiu —, ela é usada como símbolo de poder e controle. Enquanto Mare luta para resistir, a Guarda Escarlate se fortalece, unindo sanguenovos e aliados na preparação para a guerra. Entre eles está Cal, o príncipe prateado que já perdeu tudo — menos a determinação de resgatar Mare. Dividido entre o dever e o sentimento, Cal precisa escolher um lado. Em um reino à beira do caos, a liberdade tem um preço, e a rebelião está prestes a explodir.',
      preco: 49.92,
      capa: 'public/image/PrisaoDoRei.jpg',
      autor: 'Victoria Aveyard',
      contador: 1
    },
      {
      id: 17,
      titulo: 'Tempestade de guerra',
      resumo: 'Após a traição de Cal, Mare Barrow segue lutando ao lado dos rebeldes para libertar Norta. Para vencer, ela se une ao príncipe que partiu seu coração e enfrenta Maven, o rei obcecado por ela. Em meio a batalhas e sacrifícios, Mare precisa decidir até onde está disposta a ir pela liberdade.',
      resenha: 'Mare Barrow aprendeu que a liberdade tem um custo — e, às vezes, esse preço é o próprio coração. Após a traição de Cal, ela precisa reunir forças para seguir lutando ao lado dos rebeldes, determinada a derrubar Maven e libertar Norta da opressão. Para vencer essa guerra, Mare será forçada a se aliar ao príncipe que partiu seu coração, enfrentando o rei que quase a destruiu. Com os poderosos prateados de Cal e os insurgentes da Guarda Escarlate, a resistência forma uma frente unida. Mas Maven, consumido pela obsessão, fará de tudo para reconquistar Mare — mesmo que isso signifique mergulhar o reino em caos. Em meio a batalhas épicas e decisões cruéis, Mare terá que descobrir o que está disposta a sacrificar por um futuro livre.',
      preco: 55.21,
      capa: 'public/image/TempestadeDeGuerra.jpg',
      autor: 'Victoria Aveyard',
      contador: 1
    },
      {
      id: 18,
      titulo: 'Trono destruído',
      resumo: 'rono Destruído é uma coletânea imperdível para os fãs de Victoria Aveyard, trazendo seis contos que expandem o universo de Mare Barrow. Além das histórias já conhecidas, como "Canção da Rainha" e "Cicatrizes de Aço", o livro inclui quatro narrativas inéditas, explorando o passado de personagens e as consequências da guerra. Uma despedida emocionante e cheia de novos detalhes do mundo de Norta.',
      resenha: 'Trono Destruído é uma coletânea imperdível para os fãs da série best-seller de Victoria Aveyard que não estavam prontos para se despedir do universo de Mare Barrow. Com design especial e conteúdo exclusivo, o livro reúne seis contos — incluindo os já conhecidos “Canção da Rainha” e “Cicatrizes de Aço”, além de quatro histórias inéditas. Cada narrativa oferece novas perspectivas, revelando detalhes sobre o passado de personagens marcantes, explorando as consequências da guerra e apresentando rostos novos que expandem ainda mais o universo de Norta. Uma despedida poderosa e emocionante para quem deseja retornar, por mais um instante, ao mundo dividido por sangue e poder.',
      preco: 49.81,
      capa: 'public/image/TronoDestruido.jpg',
      autor: 'Victoria Aveyard',
      contador: 1
    },
      {
      id: 19,
      titulo: 'Ninguém vai te ouvir gritar',
      resumo: 'A Academia Masters, um prestigiado internato secreto na Flórida, esconde mais do que apenas alunos de elite. Quando Calvin, filho do secretário de estado, desaparece misteriosamente, deixando um bilhete com um aviso enigmático, seu irmão Andrew se vê envolvido em uma teia de segredos e ameaças. A verdadeira prova da escola não está nos estudos, mas nas sombras que a envolvem.',
      resenha: 'A Academia Masters é um dos internatos mais prestigiados dos EUA — e também um dos mais secretos. Localizada em uma ilha isolada na costa da Flórida e cercada por muros impenetráveis, a escola abriga não só alunos de elite, mas também segredos obscuros. Entre os novatos de 2022 estão Andrew e Calvin, filhos do secretário de estado norte-americano. Na primeira noite, Calvin desaparece misteriosamente, deixando apenas um bilhete ensanguentado com um aviso críptico sobre algo — ou alguém — cujo nome começa com "L". Ignorado pelos adultos, Andrew se vê sozinho em uma rede perigosa de segredos, pistas e ameaças. Ele logo percebe que a verdadeira prova da Academia não está nas salas de aula, mas nas sombras que a cercam.',
      preco: 34.75,
      capa: 'public/image/NinguemVaiTeOuvir.jpg',
      autor: 'Mark Miller',
      contador: 1
    },
     {
      id: 20,
      titulo: 'Morando com um vampiro',
      resumo: 'Cassie Greenberg, uma artista em dificuldades financeiras, encontra um quarto para alugar com um preço inacreditável e divide o apartamento com o excêntrico Frederick J. Fitzwilliam, um homem misterioso que vive à noite. Quando descobre bolsas de sangue na geladeira, Frederick revela seu segredo: é um vampiro, e faz uma proposta que pode mudar a vida de Cassie para sempre',
      resenha: 'Cassie Greenberg ama arte, mas viver dela não tem sido fácil. Quase sem dinheiro e prestes a ser despejada, ela encontra um quarto para alugar em uma localização perfeita — e por um preço inacreditável. Desconfiada, mas sem opções, aceita dividir o apartamento com Frederick J. Fitzwilliam, um homem excêntrico que dorme durante o dia, sai à noite e fala como se fosse de outro século. Aos poucos, Cassie se surpreende com sua gentileza, apoio e... aparência sem camisa. Tudo parece estar indo bem — até ela encontrar bolsas de sangue na geladeira. Frederick, então, revela seu segredo: é um vampiro. E tem uma proposta que pode mudar a vida de Cassie para sempre.',
      preco: 45.57,
      capa: 'public/image/MorandoComUmVampiro.jpg',
      autor: 'Jenna Levine',
      contador: 1
    },
     {
      id: 21,
      titulo: 'Império do Vampiro',
      resumo: 'Há 27 anos, o sol desapareceu, e os vampiros dominaram a Terra, instaurando um império de trevas. Gabriel de León, meio humano e meio monstro, é o último Santo de Prata, um guerreiro treinado para caçar vampiros. Capturado, ele narra sua jornada repleta de batalhas, amores proibidos e a busca pelo Santo Graal, a última esperança de salvação. Império do Vampiro é o primeiro volume da série dark fantasy de Jay Kristoff.',
      resenha: 'Há 27 anos, o sol desapareceu — e, desde então, os vampiros conquistam a Terra, dizimando a humanidade e instaurando um império de trevas. Em meio à escuridão, poucas faíscas de resistência ainda brilham. Gabriel de León, meio humano e meio monstro, é o último Santo de Prata — um guerreiro sagrado treinado para caçar vampiros. Agora, capturado por seus inimigos, Gabriel é forçado a narrar sua trajetória: uma saga de batalhas sangrentas, amores proibidos, fé em ruínas e a eterna busca pelo lendário Santo Graal — a única esperança de salvação. Império do Vampiro é o primeiro volume da nova série dark fantasy de Jay Kristoff, ilustrado por Bon Orthwick e destinado a se tornar um clássico sombrio do gênero.',
      preco: 86.56,
      capa: 'public/image/ImperioVampiro.jpg',
      autor: 'Jay Kristoff',
      contador: 1
    },
      {
      id: 22,
      titulo: 'Luar da Feiticeira de Ossos',
      resumo: 'Em um mundo onde somente as Feiticeiras de Ossos podem manter os mortos afastados, Ailesse deve cumprir um destino sombrio: encontrar o amor verdadeiro e matá-lo em até um ano. Bastien, em busca de vingança pela morte do pai, vê seus destinos se entrelaçarem com o dela. Enquanto isso, Sabine tenta salvar sua melhor amiga, em meio a magia, romance impossível e uma traição que ameaça romper a barreira entre vivos e mortos. Luar da Feiticeira de Ossos é o primeiro volume de uma duologia cheia de mistério e emoção.',
      resenha: 'Somente as Feiticeiras de Ossos podem manter os mortos longe do mundo dos vivos. Mas esse poder exige sacrifício: para concluir seu rito, elas devem encontrar o amor verdadeiro — e matá-lo em até um ano. Ailesse sempre foi preparada para liderar sua irmandade, mas antes precisa cumprir seu destino sombrio. Bastien, marcado pela morte do pai nas mãos de uma feiticeira, busca vingança, mas seu plano falha quando seus destinos se entrelaçam. Enquanto isso, Sabine, que nunca quis esse poder, fará de tudo para salvar sua melhor amiga. Luar da Feiticeira de Ossos é o primeiro volume de uma duologia repleta de magia, romance impossível e uma traição capaz de romper a barreira entre vivos e mortos.',
      preco: 42.14,
      capa: 'public/image/LuarDaFeiticeira.jpg',
      autor: 'Kathryn Purdie',
      contador: 1
    },
      {
      id: 23,
      titulo: 'Uma janela sombria',
      resumo: 'Em Blunder, um reino amaldiçoado, Elspeth Spindle carrega um espírito sombrio, o Pesadelo, que a protege, mas cobra um preço alto. Quando ela se encontra com Ravyn Yew, capitão da Guarda Real, ambos se unem para encontrar as doze Cartas da Providência e libertar o reino. Enquanto a atração entre eles cresce, Elspeth deve decidir se pode confiar em Ravyn, ao mesmo tempo em que luta contra o Pesadelo que ameaça devorar sua mente e alma. Uma história de magia sombria, desejo perigoso e sacrifícios inevitáveis.',
      resenha: 'Para sobreviver no reino amaldiçoado de Blunder, Elspeth Spindle precisa esconder o Pesadelo — um antigo espírito sombrio preso em sua mente. Ele a protege… mas exige um preço. Quando Elspeth cruza o caminho de Ravyn Yew, capitão da Guarda Real e sobrinho do rei, é arrastada para um plano ousado para libertar o reino da maldição que o envolve. Juntos, precisam encontrar as doze Cartas da Providência, relíquias mágicas capazes de trazer a cura. À medida que a atração entre os dois cresce, Elspeth precisa decidir se pode confiar em Ravyn — enquanto luta contra a presença crescente do Pesadelo, que ameaça consumir sua mente e alma. Uma história de magia sombria, desejo perigoso e sacrifícios inevitáveis.',
      preco: 52.18,
      capa: 'public/image/UmaJanelaSombria.jpg',
      autor: 'Rachel Gillig',
      contador: 1
    },
      {
      id: 24,
      titulo: 'Quarta asa',
      resumo: 'Violet Sorrengail, aos 20 anos, é forçada por sua mãe, a temida general de Navarre, a competir por um lugar entre os cavaleiros de dragões no Instituto Militar Basgiath, onde a morte é quase certa para os fracos. Menor e mais frágil que os outros cadetes, Violet enfrenta inimigos, incluindo Xaden Riorson, o líder de esquadrão, e precisa usar sua inteligência para sobreviver. Em meio a traições, alianças e uma guerra iminente, Violet descobrirá segredos que podem mudar o destino do reino',
      resenha: 'Violet Sorrengail, de vinte anos, deveria seguir uma vida tranquila entre livros como escriba. Mas sua mãe, a temida general de Navarre, a obriga a entrar no Instituto Militar Basgiath e disputar um lugar entre os cavaleiros de dragões — onde a morte é quase certa para os fracos. Menor e mais frágil que os demais cadetes, Violet sabe que um passo em falso pode virar cinzas. Com menos dragões do que candidatos, muitos fariam de tudo para vê-la morta, especialmente por ser filha da comandante. Entre eles está Xaden Riorson, o perigoso líder de esquadrão. Cercada por traições, alianças improváveis e perigos crescentes, Violet precisa usar sua inteligência para sobreviver — e descobrir o que a liderança esconde enquanto a guerra se aproxima.',
      preco: 56.08,
      capa: 'public/image/QuartaAsa.jpg',
      autor: 'Rebecca Yarros',
      contador: 1
    },
      {
      id: 25,
      titulo: 'Noiva',
      resumo: 'Misery Lark, vampira renegada, é forçada a se casar com o alfa Lowe para selar a paz entre espécies. Ela esconde motivos pessoais por trás do acordo, buscando recuperar algo precioso. Entre traições e atração proibida, nasce um romance que desafia seus mundos',
      resenha: 'Misery Lark, filha do vampiro mais poderoso do sudoeste, sempre viveu à margem de sua espécie. Quando é chamada a firmar um acordo de paz entre vampiros e licanos, ela é forçada a se casar com Lowe Moreland, o alfa de um bando de lobisomens. Lowe governa com autoridade, mas não confia em Misery — e ele está certo. A vampira tem motivos secretos para aceitar o casamento, algo que nada tem a ver com política, mas com o que ela mais preza no mundo. Disposta a fazer o que for preciso para recuperar o que perdeu, ela se vê, porém, atraída por seu inimigo. E ele, contra suas intenções, também sente a mesma atração. Noiva é uma história de paixões inesperadas, traições e desejos proibidos.',
      preco: 44.75,
      capa: 'public/image/Noiva.jpg',
      autor: 'Ali Hazelwood',
      contador: 1
    },
     {
      id: 26,
      titulo: 'Odeio te amar',
      resumo: 'Mara, Sadie e Hannah são cientistas que enfrentam dilemas amorosos com homens que desafiam sua lógica e sentimentos. Entre heranças complicadas, reencontros dolorosos e sobrevivência no Ártico, elas descobrem que a química vai além dos laboratórios. Amor, teoricamente mostra que, às vezes, o coração ignora até as leis da ciência.',
      resenha: 'Mara, Sadie e Hannah são cientistas brilhantes e melhores amigas que tentam equilibrar razão e emoção — especialmente quando o amor desafia a lógica. Mara, engenheira ambiental, herda uma casa... mas com um problema: terá que dividi-la com Liam, um advogado petroleiro irritante e irresistível. Sadie, engenheira civil, reencontra Erik — o homem que partiu sua confiança — presos juntos em um elevador. Já Hannah, engenheira da Nasa, sofre um acidente no Ártico e depende de Ian, o homem que quase arruinou sua carreira, para sobreviver. Em Amor, teoricamente, opostos se atraem, a química é real e nem sempre a ciência tem todas as respostas.',
      preco: 36.77,
      capa: 'public/image/OdeioTeAmar.jpg',
      autor: 'Ali Hazelwood',
      contador: 1
    },
     {
      id: 27,
      titulo: 'A hipótese do Amor',
      resumo: 'Olive Smith, aluna de doutorado, inventa um namoro para ajudar sua melhor amiga e acaba beijando o temido professor Adam Carlsen. Surpreendentemente, ele aceita manter a farsa, e o que era mentira começa a parecer real demais. Em meio a dados e experimentos, Olive descobre que o amor é a variável mais imprevisível.',
      resenha: 'Olive Smith é aluna de doutorado em Biologia em Stanford e acredita firmemente em dados, estatísticas e experimentos — não em sentimentos descontrolados como o amor. Para ajudar sua melhor amiga a ficar com Jeremy, um ex-caso sem importância, Olive inventa que está em um novo relacionamento. Mas cientistas precisam de provas, e, em um impulso, ela beija o primeiro homem que vê: Adam Carlsen, o temido e brilhante professor da universidade. Para sua surpresa, ele concorda em manter a farsa. Só que o que começou como um experimento social vira algo fora de controle, e Olive vai descobrir que, mesmo com toda a lógica do mundo, o amor pode ser a variável que muda tudo.',
      preco: 45.03,
      capa: 'public/image/AHipotese.jpg',
      autor: 'Ali Hazelwood',
      contador: 1
    },
     {
      id: 28,
      titulo: 'A razão do amor',
      resumo: 'Bee tem a chance de liderar um projeto da NASA, mas precisa trabalhar com Levi, seu antigo rival do doutorado. Apesar da tensão entre eles, ela começa a notar sinais inesperados de apoio — e de algo mais. Entre ciência e sentimento, Bee precisa decidir se segue a razão ou arrisca tudo pelo amor.',
      resenha: 'A carreira de Bee Königswasser está por um fio, até que surge a chance de liderar um projeto de neuroengenharia da NASA. Inspirada por Marie Curie, ela decide aceitar o desafio — mesmo sabendo que terá que trabalhar com Levi Ward, seu rival da época do doutorado. Levi é brilhante, alto, de olhos verdes hipnotizantes... e já deixou claro que preferiria vê-la em outra galáxia. Mas, conforme o projeto avança, Bee começa a perceber sinais confusos: Levi parece apoiá-la, valoriza suas ideias — e a olha de um jeito nada científico. Será seu cérebro pregando peças ou há algo a mais por trás daquele olhar? Quando o coração começa a acelerar, Bee precisa escolher: seguir a lógica ou arriscar tudo pelo improvável?',
      preco: 40.83,
      capa: 'public/image/ARazao.jpg',
      autor: 'Ali Hazelwood',
      contador: 1
    },
    {
      id: 29,
      titulo: 'Assistente do Vilão ',
      resumo: 'Evie Sage, desesperada por um emprego, aceita a vaga de assistente do temido Vilão de Rennedawn, mesmo sabendo dos riscos. Embora sua personalidade otimista não combine com o caos e violência ao redor, ela logo se vê envolvida em uma conspiração para sabotar o império sombrio do Vilão. Além de lidar com seu crescente interesse por ele, Evie precisa desvendar o mistério antes que sua vida (e coração) estejam em perigo.',
      resenha: 'PROCURA-SE ASSISTENTE: Vilão poderoso busca apoio para funções obscuras e caos aleatório. Benefícios excelentes. Discrição obrigatória.Evie Sage está desesperada por um emprego. Então, quando esbarra acidentalmente com o Vilão mais temido de Rennedawn e ele a contrata, ela aceita na hora. Mesmo sendo alegre e otimista demais para um ambiente cheio de decapitações, Evie está disposta a se adaptar — especialmente quando seu novo chefe é aterrorizante... e incrivelmente gato. Mas logo ela percebe que alguém está tentando sabotar o império sombrio do Vilão. Agora, além de esconder sua queda por ele, Evie precisa descobrir quem está por trás da conspiração antes que seu emprego (e seu coração) sejam destruídos.',
      preco: 38.86,
      capa: 'public/image/AssitenteDoVilao.jpg',
      autor: 'Hannah Nicole Maehrer',
      contador: 1
    },
     {
      id: 30,
      titulo: 'De sangue e cinzas',
      resumo: 'Poppy, prestes a completar 19 anos, deve cumprir seu destino como Donzela de Solis e salvar o reino, embora não entenda o que isso implica. Quando Hawke Flynn entra em sua vida, ela se vê envolvida em mentiras, traições e desejos proibidos. Agora, precisa decidir em quem confiar, pois o destino de dois reinos depende dela.',
      resenha: 'Poppy, prestes a completar 19 anos, se prepara para sua Ascensão — um destino que não escolheu e que a entrega aos deuses. Como a Donzela de Solis, ela está destinada a salvar o reino dos Atlantes e seus Vorazes, mas Poppy não entende o que isso realmente significa. Privada de escolhas e vivendo uma vida solitária, ela sonha em lutar ao lado dos guardas contra as criaturas que mataram seus pais. Quando o misterioso Hawke Flynn entra em sua vida, Poppy se vê em uma teia de mentiras, traições e desejos proibidos. Agora, ela precisa decidir em quem confiar, pois o destino de dois reinos depende dela.',
      preco: 54.82,
      capa: 'public/image/DeSangueECinzas.jpg',
      autor: 'Jennifer L. Armentrout',
      contador: 1
    },
     {
      id: 31,
      titulo: 'A mecânica do amor',
      resumo: 'Bel, sem rumo após o colégio, se junta ao clube de robótica e se vê em rivalidade com Teo, o líder popular. Trabalhando juntos, Teo reconhece o talento de Bel e começa a se interessar por ela. Entre competição e amizade, eles enfrentam sentimentos inesperados.',
      resenha: 'Bel não sabe o que fazer após se formar no colégio, mas quando revela um talento para engenharia, é incentivada por uma professora a se juntar ao clube de robótica. O problema é que o clube é comandado por Teo, um garoto inteligente, popular e com o futuro planejado. O choque é imediato: eles se odeiam. Porém, ao trabalharem juntos em robôs de combate, Teo começa a reconhecer o talento de Bel e se vê cada vez mais atraído por ela, até começando a aprender a discografia de Taylor Swift, sua cantora favorita. Entre rivalidade e amizade, os dois terão que lidar com sentimentos inesperados.',
      preco: 37.44,
      capa: 'public/image/AMecanica.jpg',
      autor: 'Alexene Farol Follmuth',
      contador: 1
    },
     {
      id: 32,
      titulo: 'História é tudo que me deixou',
      resumo: 'Quando Theo, o primeiro amor de Griffin, morre em um acidente, seu mundo desaba, pois ele sempre acreditou que Theo voltaria para ele. Agora, com o apoio de Jackson, o namorado atual de Theo, Griffin lida com compulsões e escolhas destrutivas. Para seguir em frente, ele precisa enfrentar seus próprios segredos e confrontar as lembranças de Theo antes que elas o consumam',
      resenha: 'Quando Theo, o primeiro amor e ex-namorado de Griffin, morre afogado em um acidente, seu mundo desmorona. Embora Theo tenha se mudado para a Califórnia e começado a namorar Jackson, Griffin sempre acreditou que ele voltaria para ele. Agora, o futuro que ele imaginava está destruído. Para piorar, a única pessoa que entende sua dor é Jackson, mas, mesmo com o apoio dele, Griffin se afunda em compulsões e escolhas destrutivas. Para reconstruir sua vida, Griffin precisará confrontar suas lembranças com Theo e enfrentar seus próprios segredos antes que eles o consumam.',
      preco: 46.35,
      capa: 'public/image/HistoriaETudo.jpg',
      autor: 'Adam Silveira',
      contador: 1
    },
     {
      id: 33,
      titulo: 'Para sempre',
      resumo: 'Após salvar o reino de um imperador tirano, Arek aceita temporariamente o trono, mas descobre que a princesa legítima está morta. Agora, ele precisa escolher um cônjuge antes de completar 18 anos para evitar um destino trágico. Em meio a magia, poder e desafios, Arek e seu melhor amigo Matt enfrentam uma jornada de descobertas, sentimentos inesperados e muito humor.',
      resenha: 'Após salvar o reino de um imperador tirano, Arek aceita temporariamente o trono até que a legítima herdeira possa assumir. Porém, ao chegar ao local onde ela estava presa, descobre que a princesa está morta há anos. Agora, Arek deve escolher um cônjuge antes de completar 18 anos, ou terá o mesmo destino trágico. Em um reino cheio de magia, poder e desafios para governar, Arek e seu melhor amigo Matt enfrentam uma jornada de descobertas, sentimentos inesperados e, claro, muito humor. No fim, o amor pode precisar apenas de um empurrão do destino.',
      preco: 27.44,
      capa: 'public/image/ParaSempre.jpg',
      autor: 'F.T. Lukens',
      contador: 1
    },
     {
      id: 34,
      titulo: 'A filha do rei pirata',
      resumo: 'A capitã Alosa, filha do rei pirata, se deixa capturar pela tripulação inimiga para recuperar um mapa perdido que leva a um tesouro. No entanto, o pirata Riden, charmoso e mordaz, se torna seu maior obstáculo. Em uma aventura cheia de adrenalina, Alosa usará todos os seus truques para alcançar seu objetivo.',
      resenha: 'A capitã Alosa, ousada e destemida, é enviada em uma missão para recuperar um mapa perdido, a chave para o tesouro mais procurado dos mares. Para isso, ela se deixa capturar pela tripulação inimiga, mas não esperava que o pirata Riden, charmoso e mordaz, fosse o maior obstáculo em seu caminho. Em uma aventura cheia de adrenalina, Alosa usará todos os seus truques para alcançar seu objetivo. Mas ela não é uma qualquer; filha do rei pirata, ninguém pode impedi-la de conquistar o que deseja.',
      preco: 55.92,
      capa: 'public/image/AFilhaDoRei.jpg',
      autor: 'Tricia Levenseller',
      contador: 1
    },
     {
      id: 35,
      titulo: 'Vermelho, branco e sangue azul',
      resumo: 'Alex Claremont-Diaz, filho da presidenta dos EUA, é o queridinho da mídia e tem futuro político promissor, mas ao ser forçado a interagir com o príncipe britânico Henry, ele enfrenta uma série de desentendimentos. Após um encontro desastroso, os dois fingem ser amigos para evitar um escândalo diplomático. No entanto, essa amizade começa a se transformar em algo inesperado, desafiando suas próprias identidades e expectativas.',
      resenha: 'Alex Claremont-Diaz, filho da presidenta dos Estados Unidos, é o queridinho da mídia e tem tudo para seguir carreira política. Porém, quando sua família é convidada para o casamento real britânico, ele precisa lidar com Henry, o príncipe britânico que ele não suporta. O encontro deles é um desastre, e todos os jornais do mundo estampam fotos insinuando uma briga. Para evitar um escândalo diplomático, Alex e Henry fingem ser amigos. Mas, ao longo do fim de semana, essa amizade começa a evoluir para algo inesperado, desafiando tudo o que eles imaginavam sobre si mesmos.',
      preco: 36.98,
      capa: 'public/image/VermelhoBranco.jpg',
      autor: 'Casey McQuiston',
      contador: 1
    },
     {
      id: 36,
      titulo: 'Cinderela está morta',
      resumo: 'Dois séculos após Cinderela, o reino de Mersailles é dominado por tiranos. Sophia, sonhando em se casar com sua amiga Erin, foge para o mausoléu de Cinderela, onde encontra uma aliada inesperada. Juntas, elas enfrentam o regime opressor em busca de liberdade.',
      resenha: 'Dois séculos após a história de Cinderela, a magia desapareceu e o reino de Mersailles é dominado por reis tirânicos. No Baile Anual, as jovens devem ser escolhidas como esposas ou enfrentar a ruína. Sophia, prestes a participar do baile, sonha em se casar com sua melhor amiga, Erin. No dia do evento, ela decide fugir e se refugia no mausoléu de Cinderela, onde encontra uma aliada inesperada. Juntas, elas desvendam os mistérios das lendas e enfrentam o regime opressor do rei, lutando por liberdade em uma sociedade patriarcal.',
      preco: 25.99,
      capa: 'public/image/Cinderela.jpg',
      autor: 'Kalynn Bayron',
      contador: 1
    },
     {
      id: 37,
      titulo: 'Asas reluzentes',
      resumo: 'Clarion, fada da Primavera, entra no Bosque do Inverno para investigar rumores de um monstro. Lá, conhece Milori, um guardião do Inverno com quem forma um laço improvável. Mas sua união pode ser tão perigosa quanto a ameaça que enfrentam.',
      resenha: 'Clarion, uma fada das estações quentes prestes a ser coroada, sempre foi fascinada pelo misterioso Bosque do Inverno, embora fadas como ela evitem cruzar suas fronteiras. Quando rumores sobre um monstro vindo do Inverno ameaçando a Primavera chegam ao palácio, Clarion vê a chance de provar seu valor. No entanto, em vez de um monstro, ela encontra Milori, um jovem guardião do Inverno. Unidos por um objetivo em comum, eles formam um laço improvável. Mas, à medida que esse vínculo se aprofunda, Clarion e Milori descobrem que a união entre suas estações pode ter consequências perigosas – talvez tão letais quanto os próprios monstros do inverno.',
      preco: 55.93,
      capa: 'public/image/AsasReluzentes.jpg',
      autor: 'Allison Saft',
      contador: 1
    },
     {
      id: 38,
      titulo: 'Luzes do Norte',
      resumo: 'Dimitria, caçadora renomada, é contratada para proteger Aurora, herdeira de uma família poderosa. A missão se complica quando sentimentos entre as duas surgem, ameaçando o coração do irmão de Dimitria e seu próprio futuro. Enquanto isso, um monstro perigoso assombra a floresta.',
      resenha: 'Dimitria Coromandel é a melhor caçadora de Nurensalem e sustenta sua família desde a morte dos pais. Quando é contratada para proteger Aurora, filha da influente família Van Vintermer, sua rotina muda drasticamente. Agora, além de garantir segurança à jovem, ela ganha um salário que garante conforto ao irmão Gui, secretamente apaixonado por Aurora. Mas a convivência entre Dimitria e a protegida desperta sentimentos inesperados e perigosos. Enquanto tenta equilibrar o dever com o desejo, proteger seu emprego e o coração do irmão, Dimitria ainda precisa enfrentar uma ameaça real: um monstro que ronda as florestas e ataca crianças. Em meio a dilemas morais e perigos iminentes, ela terá que decidir o que está disposta a sacrificar',
      preco: 40.84,
      capa: 'public/image/LuzesDoNorte.jpg',
      autor: 'Giulianna Domingues',
      contador: 1
    },
     {
      id: 39,
      titulo: 'Vergonha',
      resumo: 'Grace retorna à sua cidade natal para se curar da traição do marido e encontra consolo em Jackson, o rebelde local. O que começa como distração se transforma em algo mais profundo. Agora, ela precisa decidir entre o passado seguro e um futuro incerto.',
      resenha: 'Grace Harris está de coração partido após ser traída pelo marido e decide passar o verão em sua cidade natal, Chester, buscando paz e recomeço. Lá, inesperadamente, encontra conforto em Jackson Emery, o "bad boy" da cidade, marcado por perdas e com fama de encrenca. Unidos pela dor e pela solidão, eles se aproximam em um relacionamento sem promessas, apenas uma distração passageira. No entanto, à medida que o verão avança, os sentimentos se intensificam e Grace percebe que algumas conexões, por mais improváveis que pareçam, deixam marcas profundas — e exigem decisões difíceis sobre amor, perdão e o próprio futuro.',
      preco: 41.14,
      capa: 'public/image/Vergonha.jpg',
      autor: 'Brittainy Cherry',
      contador: 1
    },
     {
      id: 40  ,
      titulo: 'Sonho e Pesadelo',
      resumo: 'Criados como opostos, Sonho e Pesadelo jamais deveriam se encontrar. Mas quando ele escapa de seu cativeiro, nasce entre eles uma conexão inesperada. Juntos, precisam enfrentar os deuses e descobrir que talvez equilíbrio venha da união, não da separação.',
      resenha: 'No universo onde tudo nasce em pares, a deusa Sonho foi criada para nunca se aproximar de sua metade divina, o deus Pesadelo. Filha de Esperança e Vontade, ela representa a luz, enquanto ele, nascido de Angústia e Medo, representa as sombras. Movido pelo ressentimento, Pesadelo rompe as correntes que o aprisionam, disposto a se vingar de Sonho. No entanto, o encontro entre os dois desencadeia uma conexão inesperada. Entre encontros secretos, questionamentos sobre suas origens e sentimentos proibidos, ambos precisam desafiar os deuses que os criaram para restaurar o equilíbrio do mundo — e descobrir que, juntos, são mais do que apenas opostos.',
      preco: 48.12,
      capa: 'public/image/SonhoEPesadelo.jpg',
      autor: 'Marina Dutra',
      contador: 1
    },
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
const livrosFiltrados = computed(() => {
  if (!inputValue.value.trim()) {
    return listaLivros.value
  }
  return listaLivros.value.filter(livro =>
    livro.titulo.toLowerCase().includes(inputValue.value.toLowerCase())
  )
})
function decrementarlixeira(index){
  if (index >= 0 && index < listaCarrinho.value.length) {
    listaCarrinho.value.splice(index, 1);
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
            <FontAwesomeIcon class="iconePesquisa" icon="magnifying-glass" @click=" telaAtual = 'pesquisa'" />
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
      <div v-if="inputValue.trim() !== ''" class="principal-pesquisa">
        <section class="pesquisa">
          <ul>
            <li v-for="livro in livrosFiltrados" :key="livro.id" class="livro-item">
              <img :src="livro.capa" alt="Capa do livro" width="200" height="280" />
              <h3>{{ livro.titulo }}</h3>
              <p>{{ livro.autor }}</p>
              <p>R$ {{ livro.preco }}</p>
              <div>
                    <button @click="adicionarCarrinho(livro)"
                :class="listaCarrinho.some(item => item.id === livro.id) ? 'btn-adicionado' : 'btn-comprar'"
                style="cursor: pointer;">
                <FontAwesomeIcon icon="cart-shopping" />
                {{listaCarrinho.some(item => item.id === livro.id) ? 'Adicionado' : 'Comprar'}}
              </button>
              <FontAwesomeIcon :icon="[favoritos.includes(livro.id) ? 'fas' : 'far', 'heart']"
                  @click="adicionarFavoritos(livro.id)"
                  style="cursor: pointer; margin-left: 1rem; color: #2e649e; font-size: 1.02rem;" />
              </div>

            </li>
          </ul>
        </section>

      </div>
      <div v-if="telaAtual === 'loja' && inputValue.trim() === ''">
        <section class="random" style="display: flex; align-items: center;">
          <div>
            <p class="autor">{{ livroEscolhido.autor }}</p>
            <p class="titulo"> {{ livroEscolhido.titulo }}</p>
            <p class="resumo">{{ livroEscolhido.resumo }}</p>
            <button @click="abaLivros(livroEscolhido)">Acessar página do livro</button>
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

      <div v-if="listaCarrinho.length == 0 && telaAtual === 'carrinho' && inputValue.trim() === ''" class="carrinho-vazio">
        <p>
          <img src="https://cdn-icons-png.flaticon.com/512/11010/11010851.png" alt="Carrinho" width="120px">
        </p>
        <p style="font-size: 2.1rem; font-weight: 700; ">Seu carrinho está vazio</p>

        <p>
          <button @click="telaAtual = 'loja'">Voltar para a loja</button>
        </p>

      </div>

      <div v-if="telaAtual === 'carrinho' && listaCarrinho.length > 0 && inputValue.trim() === ''" style="display: flex; ">
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
                  <div style="display: flex; align-items: center;">
                     <div class="button" style="display: flex; align-items: center;">
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
                    <button class="lixeira" @click="decrementarlixeira(index)">
                      <span class="fa-solid fa-trash-can"></span>
                    </button>
                  </div>
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
      <section v-if="telaAtual === 'abaLivros' && inputValue.trim() === ''" class="aba-livro">
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
        <button @click="telaAtual = 'loja'" class="voltar">Voltar</button>
      </section>

      <section v-if="telaAtual === 'favoritos' && favoritos.length == 0 && inputValue.trim() === ''" class="favoritosVazio">
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
  width: 30%;
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
section.carrinho .lado{
  align-items: center;
}
section.carrinho .button {
  padding: 3px 20px;
  border: 2px solid #4F4C57;
  margin: 0 0.5vw 0 3vw ;
  font-size: 1.01rem;
  font-weight: 600;
}
section.carrinho .lixeira{
  border: none;
  background-color: white;
  font-size: 1.2rem;
  margin-right: 5vw;
  font-weight: 500;
}
section.carrinho .lixeira:hover{
  color: #4a88cb;
  transition: 0.5s;
  scale: 1.1;
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
  font-size: 1.1rem;
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

section.aba-livro .informacoes {
  display: flex;
  justify-content: space-between;
  margin: 3vw 8vw;
  border: #4a88cb 2px solid;
  padding: 2vw;
  align-items: center;
  border-radius: 5px;
}

section.aba-livro .informacoes .resumo {
  margin-left: 5vw;

}

section.aba-livro .informacoes h2 {
  font-size: 2rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
}

section.aba-livro .informacoes .resenha {
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

section.aba-livro .voltar {
  margin-left: 8vw;
  background-color: #4a88cb;
  color: white;
  border: none;
  padding: 5px 60px;
  font-size: 1.1rem;
}

div.principal-pesquisa {
  margin: auto;
}

section.pesquisa {
  margin: 2vw 5vw 0 8vw;
}

section.pesquisa ul {
  display: flex;
  flex-wrap: wrap;
  text-align: left;  
}

section.pesquisa ul li {
  align-items: center;
  width: 19%;
  margin-bottom: 2vw;  
   display: grid;
}
section.pesquisa h3{
  width: 90%;
  color: #4F4C57;
  font-weight: 600;
}
section.pesquisa button{
background-color: #4a88cb;
color: white;
border: none;
padding: 5px 40px;
margin: 1vw 0 1vw 0;
}
section.pesquisa button:hover {
  transform: scale(1.02);
  transition: all 0.5s ease;
  background-color: #70a1d6;
}

section.pesquisa button.btn-adicionado {
  background-color: #28a745;
  padding: 5px 30px;
}
</style>