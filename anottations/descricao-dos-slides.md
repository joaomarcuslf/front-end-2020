# Front-end em 2020

## Slide 1 - Título

Apresentação do conteúdo dessa apresentação, o foco maior será em organização e estruturação de CSS e JS.

## Slide 2 - Pessoal

Apresentação pessoal.

## Slide 3 - Tópicos a serem discutidos

Apresentando os temas.

Vamos falar de CSS, falar um pouco sobre os pré-processadores, sobre flexbox e alguns modelos de organização de CSS.

Sobre JS nós vamos falar sobre alguns modelos de organização, sobre algumas lib muito úteis e dos Frameworks principais.

E finalmente algumas dicas e Hacks sobre ambos.

O repositório dessa apresentaçãotá aqui no github, eu deixei aberto alguns branchs mostrando alguns exemplos sobre os modelos de organização de CSS que vou falar.

## Slide 4 - CSS

Vamos começar com CSS.

CSS como a maioria conhece é uma linguagem focada em estilização, porém costuma trazer muitas dores de cabeça, e eu quero mostrar algumas formas de evitar essas dores...

## Slide 5 - SCSS / Less

Começando com SCSS e Less, que são dois Pré-processadores muito utilizado na área, Eles trazem muitos recursos para permitir uma escrita mais estruturada, como Variáveis, Mixins, Alinhamento de estilos e outros.

Como não é padrão do navegador, nós precisamo utilizar algumas ferramentas para build dos assets, eu citei aqui Gulp, Grunt e Webpack, pois ainda são as mais utilizadas.

## Slide 6 - Flexbox

Outra dificuldade muito comum é escrever CSS responsivo, sem ter que meter várias media queries.

Para isso nós temos Flexbox, um padrão criado mais recente, ele trato os layouts como elementos fluídos diferente de como nṍs costumamos trabalhar com blocos.

Flex permite que você trabalhe o layout em diversas direções, horizontal, vertical, da direita para esquerda e da esquerda para direita.

Eu deixei aqui dois links para referência:

- Primeiro, um link de referência bem completo sobre Flexbox.
- Segundo, um joguinho que explica as propriedades de uma forma bem interativa.

## Slide 7 - Como Organizar CSS

Agora sobre como organizar CSS. Eu peguei algumas metodologias bem conhecidas e que tem bastante material para seguir a partir dessa apresentação.

Da esquerda para direita as metodologias vão ficando com regras mais bem definidas e por consequência mais rígidos.

### OOCSS

- Esse já é uma metodologia motivada pelos estudos de Orientação a Objeto, tem enfoque em reaproveitamento e manutenção.
- Ele brilha muito em projetos de pequeno ou médio porte, portais, sistemas mais simples.

### BEM

- Já o BEM ele é uma metodologia bem mais completa e possui bem mais regras.
- O brilho do BEM está em projetos de médio e grande porte, com equipes grandes ou com conhecimentos variados de CSS

### ITCSS

- O ITCSS de todos é o com maior quantidade de regras, porém ele é bem versátil, podendo ser usado em conjunto com qualquer outra metodologia.
- O ITCSS é cheirosinho em projetos com temas reaproveitávei, onde você pode importar parcialmente partes dele, pode customizar as variáveis.

## Slide 8 - OOCSS - Overview

Como falei anteriormente, por aplicar OO, o OOCSS facilita a manutenção do CSS, tem bastante reaproveitamento de classes, e diminui a fragilidade do CSS.

Como desvantagem, o estilo fica preso aos elementos em tela, e como o OO trata os elementos como objetos, ele não possui soluções dentro da metologia para resolver as partes mais genéricas da página, como template, temas e etc. Sendo necessário criar uma por fora da metodologia.

## Slide 9 - OOCSS - Exemplos

Nesse slide nós temos um exemplo em SCSS, o navbar-element extende os estilos dos containers horizontais e verticais, que por sua vez ambos extendem o flex-container.

E nessa imagem tem a estrutura que utilizei, é uma estrutura bem simples já que o OOCSS não força nenhum padrão nesse sentido.

## Slide 10 - BEM - Overview

Agora vamos para o BEM, esse é um bem conhecido mais no exterior do que aqui no Brasil.

Ele aplica uma nomenclatura bem rígida para os seletores utilizando Bloco Elemento Modificador, sendo esse último opcional.

Tem desvantagem mais para aqueles que gostam de classes semânticas, e ele ele diferente do OOCSS ele te força a ter uma estrutura maior.

## Slide 11 - BEM - Exemplos

Fiz um exemplo bem rápido de uma navbar, e já pode ser visto aqui (segunda linha) como se aplica a nomenclatura.

navbar é o bloco
brand é o elemento

então forma navbar__brand

Já esse segundo bloco de elementos
Temos um modificador no primeiro navbar__link tornando ele ativo.

Na segunda imagem temos o exemplo dos estilos já alinhados com SCSS para ficar mais sucinto.

## Slide 12 - ITCSS - Overview

Já o ITCSS, que particularmente é o meu favorito.

Ele organiza o código com o formato de triângulo em camadas.

(Ir para o Slide 13)

Ele tem o mesmo defeito do BEM em precisar de estrutura, e ele pode ser bem mais complexo que o necessário para projetos pequenos.

## Slide 13 - ITCSS - Estrutura

As camadas da base que são maiores é onde a maior parte dos estilos, aqueles menos específicos serão aplicadas, e conforme você vai chegando na ponta mais fina voc?ê vai aplicar os estilos mais específicos, e com ITCSS a ideia é que se tenha cada vez menos estilos.

Cada camada tem sua responsabilidade, eu deixei na apresentação a explicação de cada camada, eu vou adiantar para algo mais prático.

## Slide 14 - ITCSS - Exemplos

No ITCSS nós aplicamos o DDD(vou falar um pouco mais depois), separando em pastas por responsabilidades.

Nessas imagens da direita, temos um exemplo do Bulma que aplica um ITCSS parcial, onde você pode importar partes dele.

O Bootstrap também aplica um formato parecido.

## Slide 15 - JS

Próximo tópico é o JS, e aqui eu vou falar menos de como fazer e mais de possibilidades, já que cada framework JS tem seu padrão.

## Slide 16 - Organização - Agnósticos

Começando por como organizar os arquivos, nós temos dois mais usados, o DDD que separa os arquivos por responsabilidade, ele é bem utilizado em alguns frameworks back-end, até o Rails usa algo parecido com.

E temos o MDA que é o favorito do pessoal do Angular, ele divide os arquivos em namespaces relacionados a um model, exemplo user, gallery. E dentro de Gallery nós também podemos ter image, uma entidade relacionada a gallery.

## Slide 17 - Organização - Não-agnósticos

Esses dois são específicos a alguns frameworks, então vamos seguir.

## Slide 18 - Libs Úteis

E separei aqui algumas libs bem utilizadas, ou que deveriam se mais utilizadas.

Moment que resolve data, um problema recorrente em JS.

Lodash que fornece muitas funções de helpers bem úteis.

Fetch API que é a API padrão de request dos navegadores.

Redux é o gerenciador de estados mais famosinho no ambiente React.

RxJS parece com o Lodash no sentido de fornecer vários helpers, porém ele tem foco maior em observables.

## Slide 19 - Frameworks

Eu citei aqui os 3 frameworks mais conhecidos, e tentei ser bem imparcial nas descrições.

Para resumir bem:

React resolve bem View, porém precisa ser composto com outras libs para resolver uma aplicação mais complexa.

Angular resolve bem uma Aplicação ponta a ponta, porém é o mais opinativo e te força a utilizar as ferramentas dele.

O Vue ele é o mais no meio do caminho, ele aplica um pouco do React e um pouco do Angular, porém é o menos expressivo desses.

## Slide 20 - Dicas

Vamos a algumas dicas bem rápidinhas.

## Slide 21 - Dicas de CSS - Úteis

Primeiro é para quanto tiver problema em seus estilos não estiverem funcionando, é possível aplica a seguinte fórmula.

ID Classe Elemento Genéricos

Como podemos vez nos exemplos.

Segunda dica eu destaquei duas, mas eu extendo a todas as pseudo classes, que eu tenho aplicado bastante e eu acho bem úteis.

## Slide 22 - Dicas de CSS - Gambiarras

Agora algumas gambiarrinhas em CSS.

Position absolute, é muito recomendado sempre aplicar dentro de elementos com position relative.

E o _ na frente de props, apenas o IE consegue ler propriedades assim, o que permite estilos específicos. Mas por favor, não usem.

## Slide 23 - Dicas de JS - Úteis

Em JS, nós temos várias funções bem legais para tratar dados. Eu marquei as mais conhecidas, mas tem algumas outras.

Segunda dica é como extrair um booleano puro em JS, é só colocar o !! na frente do valor, e ele converte para booleano.

## Slide 24 - Dicas de JS - Úteis

Terceira dica são os default values que em JS você pode atribuir valores padrões para funções.

E Promises, a coisa mais cheirosa em JS, que você pode descer valores fixos em Promise.all, dei um exemplo bem básico nessa imagem.

## Slide 25

E para fechar.

## Slide 26

Eu separei alguns tópicos adicionais que eu acho que valem a pena pesquisar mais a fundo.

## Slide 27

## Slide 28

## Slide 29
