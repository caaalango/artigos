# Como as Linguagens de Programação Funcionam?
"Master of puppets, 
I'm pulling your strings"
(Master of Puppets  - Metallica)
## Sumário

- <a href = #oqueeh> O que é uma Linguagem de Programação</a>
- <a href = #nivel> Alto Nível vs Baixo Nível</a>
- <a href = #compiladas> Compiladas vs Interpretadas</a>
- <a href = #paradigmas> Paradigmas de Programação </a>
- <a href = #comoFunciona> Funcionamento de uma Linguagem de Programação </a>
- <a href = #finalizacao> Conclusão </a>
- <a href = #bibliografia> Bibliografia </a>

## <span id = oqueeh > O que é Linguagem de Programação

No artigo passado, compreendemos o porquê do computador ser um máquina de calcular extremamente rápida e como ela funciona. Porém, uma máquina incontrolável é inútil para fins de solucionar nossos problemas cotidianos. Nesse sentido, é necessário uma forma de controlar essa máquina e fazemos isso por meio de linguagens de programação.

Linguagem de programação pode ser entendida como um conjunto formal de instruções que pode ser usado para controlar uma máquina. De modo simples, uma linguagem determina o que o computador vai fazer em cada momento e um programa é a execução concreta dessas instruções dessa linguagem. Se uma máquina fosse uma pessoa e disséssemos para ele ir de um ponto para o outro, tendo um buraco no meio do caminho, ele, inevitavelmente cairia, pois, por mais que o computador seja extremamente rápido, ele é extremamente literal na interpretação das instruções. O computador não faz julgamento crítico, ele irá executar o que foi determinado para ser executado.

Diante disso, classificar linguagens é difícil, pois cada linguagem tem suas peculiaridades e forma de ordenar o computador de fazer algo. Todavia, vamos fazer esse esforço.
<div align = "center">
<img src="https://i.postimg.cc/V68BtFSh/pc-com-linguagens-de-programa-o.webp" width = 200px>
</div>

## <span id = nivel> Alto Nível vs Baixo Nível

É difícil classificar uma linguagem como baixo nível ou alto nível sem antes saber o que significa esses termos. Para uma linguagem ser de alto nível, ela precisa estar mais próximo da linguagem humana, e, por isso, é mais fácil de ser interpretada por seres humanos. Já baixo nível pode significar o contrário, ou seja, são mais difíceis para o ser humano compreender, porém é um tipo de linguagem que permite um maior controle do hardware, por representar informações mais próximos deste.

A partir daqui pode surgir a pergunta: por que eu iria utilizar uma linguagem de baixo nível se, na maior parte das vezes, é mais difícil de programar com ela?. Não seria melhor programar com linguagens que são de fácil acesso ao ser humano? A resposta é intrigante: geralmente as linguagens de baixo nível possuem um desempenho muito melhor do que uma de alto nível. Lembre que a intenção da linguagem é comandar o computador, portanto, quanto mais próximo da linguagem humana, maior processamento será necessário para compreender o que está sendo instruído.

Considere o seguinte exemplo: numa fábrica podem existir diversos setores, desde o operacional, que efetivamente fabrica o elemento, até o administrativo, que gerencia a nível mais humano os processos da fábrica. Quando o administrativo pede que algo seja modificado, uma cadeia de processos começa até que efetivamente a produção mude. Mas se alguém do chão de fábrica desejar modificar algo no produto, ele terá rápido acesso e logo o produto será modificado. As linguagens de alto nível são como ordens vindas do administrativo, passam por longos processamentos para serem entendidas pelas máquinas, enquanto as linguagens de baixo nível são como as ordens vindas dos operários, de maneira quase imediata é realizada. O hardware é bastante difícil de ser manipulado e, assim como um operário precisa saber bem como o produto fabricado funciona para fazer uma modificação precisa, é necessário que o programador de baixo nível conheça bastante a arquitetura da máquina. Se escolhermos processamento, linguagens de nível nos servem bem, mas se quisermos agilidade e produtividade, as linguagens de alto nível são melhores para resolver problemas mais cotidianos.

É difícil, muitas vezes, saber se uma linguagem é baixo ou alto nível, mas uma outra forma de visualizar essa diferença é comparando as linguagens uma a uma, por exemplo: a linguagem javascript é mais alto nível que a linguagem C, ou então, Python é alto nível se comparado com assembly.

## <span id = compiladas>  Compiladas vs Interpretadas

Essa forma de separar é bem interessante porque entra em conceitos que não são tão simples de entender. Linguagens compiladas são aquelas em que o código escrito (por exemplo: um ```fmt.Println("Hello World")``` no Golang) é transformado diretamente em código de máquina (instruções que o processador do seu computador, por exemplo, consegue entender prontamente) antes de ser executado. Geralmente são linguagens mais rápidas, pois o código já está no formato que a máquina já pode executar. Além disso, as linguagens compiladas não possuem a necessidade do código original, pois ao final da compilação é gerado um executável que pode ser distribuído para ser executado em várias máquinas (por exemplo, um .exe no Windows). O código seria como a receita do bolo, o executável são todos os bolos fabricados por aquela receita.

Já linguagens interpretadas, o código fonte é executado linha por linha por um programa chamado interpretador. Em vez de ser convertido antecipadamente em código de máquina, o código fonte (aquele que você escreveu) é lido e executado diretamente pelo interpretador no momento da execução. Uma vantagem é que o mesmo código pode ser executado em diferentes plataformas (Windows, Linux, arquitetura X86, arquitetura ARM, etc), desde que o interpretador apropriado esteja disponível. Um exemplo de linguagem interpretada é o Python.

## <span id = "paradigmas">Paradigmas de Programação

Paradigmas de programação são conjuntos de princípios, conceitos e práticas que definem a forma como os programas são escritos e estruturados, ou seja, um paradigma de programação oferecem uma maneira de pensar na resolução do problema e oferecem ferramentas para tal, influenciando como os programadores vão abordar uma determinada tarefa. Alguns paradigmas de programação são:

- Programação Imperativa: Comandar uma máquina através de uma sequência de instruções sequenciais. Nesse caso, sabemos exatamente o que uma máquina está fazendo. Essa é uma estrutura suportada por várias linguagens, como C e Python.

- Programação Declarativa: Descreve o que deve ser feito, mas não como fazê-lo. A forma como a máquina executa, nesse caso, é abstraída. Um exemplo comum, é o SQL, que indicamos o que desejamos e a linguagem logo nos fornece o que desejamos, sem que tenhamos implementado as funções que manipulam o banco de dados.

- Programação Procedural: Extensão do Imperativo em que utiliza procedimentos ou funções para organizar a lógica do programa. Nesse caso, podemos reaproveitar código e isolar funcionamento. Novamente o C e Python suportam esse tipo de paradigma.

- Programação Funcional: Extensão da Declarativa em que se baseia no uso de funções matemáticas e evita dados mutáveis.

- Programação Orientada a Objetos: Baseia-se em definir ideias abstratas (classes) para podermos transformas em objetos concretos (objetos) que possuem comportamento esperado. Dessa forma, a classe padroniza a existência de vários objetos. Nem todas as linguagens possuem suporte a esse paradigma. O próprio Golang possui uma abordagem diferente de outras linguagens nesses aspecto.

Acima estão as descrições de alguns paradigmas utilizados nos dias atuais. É apenas uma vaga explicação sobre o que são, pois esse não é o foco do artigo. Só a título de interesse, a linguagem que utilizaremos (Go) é do paradigma imperativo.
<div align = center>
<img src = "https://i.postimg.cc/mDPvJBZM/Golang.webp" width = 200px>
</div>

## <span id = "comoFunciona">Funcionamento de uma Linguagem de Programação

Como foi visto, temos vários tipos de linguagens de programação com propósitos semelhantes e diferentes. Não há como especificar como cada linguagem funciona detalhadamente e não recomendamos que faça isso. Porém, é importante entender o "caminho das pedras", ou seja, compreender como o processo funciona, como um código fonte escrito pode se tornar algo em que o nosso computador consegue executar. Portanto, vamos dar uma pequena explicação de como ocorre o processo de tradução de um código fonte (em uma linguagem genérica) para um código em que o nosso processador possa compreender.

Quando escrevemos o nosso código fonte e queremos ver o resultado, geralmente apertamos um botão de executar ou então acionamos um comando no terminal como: ```go run arquivo.go```. No entanto, o que acontece quando fazemos isso? Geralmente passamos a responsabilidade da construção do código compilado para um conjunto de programas que é conhecido como compilador (no caso do Go). Vamos explicar o modelo de compilação.

Geralmente há duas partes principais na compilação que é a análise e a síntese. A análise consiste de verificar se a sintaxe e a semântica do programa estão corretas, isto é, ele analisa o seu programa e vê se está de acordo com aquilo que se espera em termos de sentido e escrita da linguagem. Por exemplo, não faz sentido escrever ```puts("hello world")``` em Go, pois puts não é uma função nativa do golang. Ao final da análise é gerado um código intermediário, de onde sairá o código final. Por fim, a fase de síntese onde o compilador gera o código de saída a partir da representação intermediária. Esse código de saída pode ser o código de máquina no qual o seu processador irá realizar determinada ação.
<div align = center>
<img src = "https://i.postimg.cc/V61wh5Zh/compiladorkk.webp" width = 200px>
</div>
### Fase de Análise

Abaixo são os passos que geralmente são seguidos na fase de análise.

- Análise Léxica: O código fonte é dividido em tokens que são elementos-chave, por exemplo: ```montante:=deposito+juros*30```. Os tokens seriam: ```montante, :=, deposito,+,juros,*,30```.

- Análise Sintática: Os tokens são organizados em uma estrutura que representa a organização gramatical do código, geralmente uma Árvore Sintática Abstrata (AST). Veja na imagem abaixo:

<div align = center>
<img src = "https://i.postimg.cc/NGbKtwcV/image.png" width = 300px>
<br><br>
</div>

Esta árvore é utilizada principalmente para verificar se o programa está seguindo as regras gramaticais da linguagem de programação.

- Análise Semântica: Nesta etapa, o compilador verifica se o programa faz sentido do ponto de vista semântico, como compatibilidade de tipos e escopo de variáveis, por exemplo. Após isso, geralmente temos a passagem para a síntese.

### Fase de Síntese

- Gerador de Código Intermediário: A AST é transformada em uma representação intermediária do código, que é uma versão de baixo nível do programa original. Pode ter uma variedade de formas. Além disso deve ser fácil de produzir. Ele é utilizado para otimização e para ser uma ponte entre o código fonte e o código de máquina. Um exemplo de código intermediário em que podemos pensar facilmente é o abaixo:

```
t1 = juros * 30
t2 = deposito + t1
montante = t2
```

Basicamente decompõem a operação original em algo mais simples.

- Otimização de Código Intermediário: O Código Intermediário é otimizado para melhorar o desempenho e a eficiência do código final.

- Geração de Código de Máquina: O Código Intermediário é então convertido em código de máquina específico para a plataforma alvo. Por exemplo, para a arquitetura x86 (genérico):
```
mov rax, [endereço_de_juros] ; Carrega 'juros' no registrador rax

; Multiplicar 'juros' por 30
mov rbx, 30                 ; Carrega 30 no registrador rbx
imul rax, rbx               ; Multiplica rax (juros) por rbx (30)

mov rbx, [endereço_de_deposito] ; Carrega 'deposito' em rbx

; Adicionar 'deposito' ao resultado da multiplicação
add rax, rbx               ; Adiciona rbx (deposito) a rax

; Armazenar o resultado final em 'montante'
mov [endereço_de_montante], rax ; Armazena o resultado em 'montante'

```

Os termos: ```[endereço_de_juros], [endereço_de_deposito], [endereço_de_montante]``` são os endereços na memória dessas variáveis. Esse código está na linguagem Assembly para a plataforma X86. 

- Assembler: Não é bem uma fase, mas sim a tradução das instruções mostradas acima para código binário para que o processador possa rodar o programa.

Observação: Há outras fases que foram deixadas de fora, como o Linking, que serve para linkar bibliotecas com o seu código, entre outros.

## <span id = finalizacao>Conclusão

Por fim, pode-se observar que o funcionamento de uma linguagem de programação é bastante complexo. Há outros tópicos a se abordar sobre linguagens de programação no geral, porém isso não é assunto que dê para tratar em um artigo rápido. O intuito é apenas mostrar algo que dê para criar interesse e incitar maior interesse na pesquisa. Estamos apresentando conceitos base da programação.

Por Gabriel Palitot, Revisado por Eliabe Bastos

## <span id = bibliografia> Bibliografia

Aho, A.V., Sethi, R. & Ullman, J.D. (2008). Compiladores – Princípios, Técnicas e Ferramentas. PEARSON - UNIVERSITARIOS/ KOTLER.
