# Como computadores funcionam?

*This is Major Tom to ground control
I'm stepping through the door
And I'm floating in the most peculiar way
And the stars look very different today
For here am I sitting in a tin can
Far above the world
Planet Earth is blue, and there's nothing I can do
(Space Oddity - David Bowie)*

## Sumário

- <a href = #maquinamagica> A máquina mágica</a>
- <a href = #eletronicadigital> Eletrônica digital</a>
- <a href = #tipos> Processador</a>
- <a href = #paradigmas> Memória auxiliar </a>
- <a href = #comoFunciona> Memória externa </a>
- <a href = #finalizacao> Gerenciador de bagunça </a>
- <a href = #bibliografia> Conclusão </a>
- <a href = #conclusao> Bibliografia </a>

## <span id = maquinamagica > A máquina mágica

Um computador, atualmente, é facilmente compreendido para alguns como um objeto mágico: mandamos ele fazer algo e ele rapidamente nos retorna um resultado. Talvez seja necessário mudar a forma como se pede, a fim de obtermos outros resultados. E, às vezes, permanecemos horas tentando realizar uma ação sem entender o motivo dos resultados que estamos encontrando.

Para dirigir, por exemplo, não precisamos necessariamente saber como funciona a parte mecânica do carro, mas saber o mecanismo que faz o carro parar nos faz tomar decisões melhores quando os freios não funcionam: engatamos o carro em uma macha baixa ou acionamos o freio de mão? Você não precisa necessariamente saber sobre como funciona os computadores para manipulá-lo ou até mesmo programá-lo. Mas, assim como no caso da falta de freio no carro, podemos também tomar decisões mais acertadas dependendo da situação. Se queremos buscar rapidamente um elemento de uma fila, usamos uma fila estática ou dinâmica?

Por isso, precisamos entender o que essa máquina mágica faz. Se eu pudesse descrever o computador em poucas palavras, eu falaria que o computador é uma máquina binária, que processa apenas 0 e 1, capaz de realizar rapidamente operações aritméticas por meio da eletrônica digital. Muita coisa, não? Vamos desmistificar nos próximos tópicos.

## <span id = eletronicadigital > Eletrônica digital

É comum falar de eletricidade como algo prático que acende uma lâmpada ou permite alguma estrutura mecânica funcionar. Todavia não pensamos que a eletricidade pode resolver, por si só, problemas matemáticos complexos. É nesse espírito que o computador consegue ganhar vida e então consegue realizar suas diversas funções.

Considere um dispositivo (iremos simplificar um pouco o funcionamento dessas estruturas) que, ao receber um sinal elétrico, retorna energia em um patamar constante e igual a 1. Se ele não receber energia, retorna um patamar constante e igual a 0. Os dispositivos eletrônicos trabalham com essas ondas em frequências extremamente altas. No entanto, é natural se perguntar: o que podemos fazer com tais números.

Podemos associar dois valores binários para obter outros valores. Neste sentido, chamados de portas os dispostivos eletrônicos que permitem a manipulação desses bits. Por exemplo, a porta AND, associa dois valores binários de modo que só teremos valor 1, caso as duas portas forem 1. Veja a tabela:

|  A  |  B  | A AND B |
|:---:|:---:|:-------:|
|  1  |  1  |    1    |
|  0  |  1  |    0    |
|  1  |  0  |    0    |
|  0  |  0  |    0    |


A porta OR associa dois valores binários de modo que só teremos 0 caso as duas portas forem 0. Veja a tabela:

|  A  |  B  | A OR B |
|:---:|:---:|:------:|
|  1  |  1  |    1   |
|  0  |  1  |    1   |
|  1  |  0  |    1   |
|  0  |  0  |    0   |


Enquanto a porta NOT, simplemente inverte o valor do valor binário em questão. Veja a tabela:

|  A  | NOT A |
|:---:|:-----:|
|  1  |   0   |
|  0  |   1   |

É surpreendente, mas toda a nossa computação se baseia somente nessas três portas. Essas trẽs portas permitiram construir o computador que levou o homem a lua.

Até parece que essas portas fazem operações não convencionais e que elas, a curto prazo, não irão nos ajudar. Mas veja: com apenas cinco portas conseguimos construir um comparador de bits. Veja a operação XOR entre duas entradas, A e B, e sua respectiva tabela.

XOR(A, B) = (A AND NOT B) OR (NOT A AND B)

|  A  |  B  | A XOR B |
|:---:|:---:|:-------:|
|  0  |  0  |    0    |
|  0  |  1  |    1    |
|  1  |  0  |    1    |
|  1  |  1  |    0    |


Veja que se ambos os bits forem iguais, a porta retorna 0, enquanto se os bits forem diferentes, a porta retorna 1. Criamos, então, o comparador de bits. Podemos, com essas portas, fazer todas as operaçoes aritméticas entre bits.

## Processadores

Perceba, no entanto, que processar bit a bit pode ser bastante trabalhoso. Se para construirmos um simples comparador de bits, tivemos que realizar todas essas operações, o que falar quando tivermos comparando inteiros? Para representar um número inteiro, os computadores atuais utilizam 4 bytes, cada um contendo 8 bits. Precisamos de algo mais robusto, algo que processe os elementos que estamos acostumados a lidar: números e caracteres.

É comum, neste momento, pensar: onde ficam armazenadas as informações que estão sendo processadas? Nos exemplos dados anteriormente, realmente não eram possíveies armazenar informações, apenas processá-las.

Conheça, então, o registrador, um componente eletrônico capaz de armazenar estados para poder posteriormente processar. Eles possuem tamanho limitado, conseguindo armazenar 32 bits ou 64 bits, dependendo do computador. Por causa do tamanho deles, os computadores são conhecidos como computadores de 32 bits e 64 bits. Eles são os blocos principais que formam a arquitetura do computador. Tudo vem deles, tudo vai para eles.

As informações guardadas dentro do registrador são chamadas de "palavra". Essas informações podem ser facilmente representadas por númeoros hexadecimais, visto que a "palavra" é uma sequência de bits. Por causa desses dispositivos, conseguimos representar duas informações em formato hexadecimal e armazená-las em registradores. A informação, nesse caso, pode ser armazenada e, então, processada rapidamente.

Se tivermos resolvido, portanto, o problemas, basta criar uma quantidade enorme de registradores e armazenar todas as nossas informações dentro desses componentes. Infelizmente, essa não é uma boa ideia. Registradores são extremamente caros de se produzir. Dentro do computador existem pouquíssimos registradores, podendo armazenar apenas alguns bytes de dados. Além disso, o computador precisa estar sendo alimentado por energia para que os dados permanceçam armazenados. Aumentar a quantidade de processadores não é uma boa opção.

## Memória auxiliar

Para armazenar mais informações, surgem as memórias auxiliares ou memórias RAM's, para garantir que os registradores processem grande quantidade de dados, sem que seja necessário armazenar tudo nos registradores. As memórias auxiliares são compostas de capacitores que, ao serem energizados, armazenam as informações, novamente, na forma de energia elétrica. A capacidade de armazenamento então sobe para Gigabytes. Nela iremos armazenar todas as informações necessárias para o processamento.

A memória é organizada no formato de pilha, como aquela de pratos. O computador vai colocando informações na pilha e a medida que precisa retirar alguma informação dela, é necessário tirar os últimos dados que foram colocados. Existe um registrador responsável só para controlar a posição da memória, chamado de "Stack Pointer".

Todavia, ainda temos o problema dos dados se perderem caso a alimentação elétrica cesse. Além disso, a quantidade de 8 Gb de memória não é grande para armazenar a quantidade de dados que possuimos. Armazenar dados em memória RAM seria extremamente caro também.

## Memória externa

Por fim, foram construídas as memórias de disco, onde iremos escrever e ler os dados que desejamos em um disco magnético. Os dados não irão se perder com o cessar de eletricidade. Porém, o acesso a essa memória é bem lento. Para falar de velocidade de acesso, podemos fazer as seguintes pressuposições:

Registrador > Mem.auxiliar > Mem.externa

Podemos associar o processamento de armazenamento e processamento com processo humano de pensamento. Armazenar no registrador é como armazenar na sua memória de trabalho. Armazenar na memória RAM é como armazenar na memória de longo prazo. Armazenar na memória externa é como escrever numa folha de papel seus pensamentos. Assim como funciona conosco, os computadores não precisam da memória externa para funcionar, basta haver o processador junto com a memória auxiliar. Mas para que os dados persistam, é necessário uma memória externa. O computador sem memória externa é como uma pessoa que dorme todo dia e esquece de tudo que aprendeu e, assim, vive sempre o mesmo dia.

Lembrando que o registrador sempre busca informações na memória RAM. Caso a informação não esteja na memória RAM, esta irá solicitar leitura ao disco para poder carregar as informações do disco na RAM, fazendo assim o computador acessar o dado. É semelhante a nós, pois primeiramente buscamos na nossa memória de longo prazo para buscar certa informação. Se não encontrarmos, buscamos mais informações em algo escrito.

Perceba que em nenhum momento mencionei forma diferentes de processar, estamos sempre utilizando 0's e 1's, seja no processador, seja na memória externa ou na memória externa. Tudo é 0's e 1's.

Imagine que uma estante onde alguém pode armazenar informações. Alguém pode armazenar folha por folha nessa estante, mas ficará extremamente desorganizado. Para isso, agrupamos informações semelhantes em conjuntos chamados de livros, e, assim, podemos procurar pelo livro para depois procurar pela informação.

Do mesmo modo acontece quando os computadores vão armazenar informações. Ele organiza a memória em abstrações chamadas de arquivos onde agrupam informações que possuem mesmo contexto. Se não fosse dessa forma, os dados estariam completamente desorganizados pela memória e gerenciar tais informações seria insustentável.

Atualmente, existem SSDs (unidades de estado sólido), que são dispositivos de armazenamento que usam memória flash NAND para armazenar dados, substituindo os discos rígidos mecânicos (HDDs) com várias vantagens. Sem partes móveis, os SSDs oferecem acesso mais rápido aos dados, maior durabilidade e resistência a choques. Eles são mais eficientes em termos energéticos, operam silenciosamente e geram menos calor. Com velocidades de leitura e gravação superiores, os SSDs melhoram significativamente o desempenho do sistema, especialmente em inicialização, carregamento de programas e transferência de arquivos.

## Gerenciador de bagunça

É uma bagunça de componentes, eu concordo. Quem abstrai tudo isso para tornar a organização que vemos no computador é o sistema operacional. Ele gerencia desde o elementos de hardware até a interface gráfica do usuário.

Você lembra do filme Matrix em que o mundo dos humanos é virtual? Lá, existem máquinas complexas e gigantecas, que processam tudo o que é necessário para que esse mundo virtual subsista. Da mesma forma, o sistema operacional abstrai toda essa complexidade do hardware, transformando em um ambiente onde o usuário pode ter maiores ferramentas para atuar.

## Conclusão

O computador, uma máquina binária processando 0s e 1s, é um milagre da eletrônica digital e da computação. Nele, portas lógicas fundamentais como AND, OR e NOT, realizam operações básicas que constroem funções complexas. O coração do computador, os processadores, efetua cálculos avançados, apoiados por registradores que armazenam dados temporariamente. Memórias auxiliares e externas, como RAM e SSD, respectivamente, expandem a capacidade de armazenamento e processamento. O sistema operacional integra esses componentes complexos, oferecendo uma interface simplificada e funcional para os usuários, transformando uma grandeza de processos técnicos em uma experiência de usuário coesa e intuitiva.

Por Eliabe Bastos, revisado por Gabriel Palitot.
