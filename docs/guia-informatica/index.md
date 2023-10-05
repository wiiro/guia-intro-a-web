# Desenvolvimento Web

Nesta aula iremos entender como funciona uma página htlm, seu sistema de arquivos e como podemos usando apenas usando a parte mais básica do desenvolvimento web recriar páginas de sites famosos.

Ao final da aula, vocês serão capazes de criar um site que imita a pagina inicial do instagram.

# HTML: Introdução
A Linguagem de Marcação de Hipertexto (HTML) é uma linguagem de marcação que compÕe a maior parte das páginas da internet e dos aplicativos online. Um hipertexto é um texto usado para fazer referência a outros textos, enqunato uma linguagem de marcação é composta por uma série de marcações que dizem para o Browser qual é o estilo e estrutura do documento.

## Conceitos Básicos
  - Um documento HTML é básicamente um texto com uma formatação (marcadores) em cima;
  - Os marcadores atribuem significados a partes do texto;
  - o navegador de internet tranforma esses significados em formatações;
  - Os marcadores NÃO atribuem formatações diretamente.

  abra o exemplo:

## Elementos Básicos
 - os marcadores que começam com < e terminam com > são chamados de tags;
 - quando uma tag começa apenas com o símbolo < seguido de uma palavra, ela é uma tag de abertura;
 - quando uma tag começa com os símbolos <!-- seguidos de uma palavra, ela é uma tag de fechamento;
 - em ambos os casos, a palavra é o nome da tag.
 - a parte do texto entre uma tag de abertura e sua tag de fechamento correspondente é o conteúdo dessas tags;
 - o trio formado por tag de abertura, tag de fechamento e conteúdo é chamado de elemento;
 - quando um elemento está dentro de outro, chamamos o externo de pai ou contêiner e chamamos o interno de filho;
 - elementos com o mesmo pai são chamados de irmãos;
 - atributos são expressões que podemos escrever em uma tag de abertura - para adicionar ou modificar propriedades do elemento;
 - geralmente, um atributo é escrito na forma CHAVE="VALOR";
 - algumas tags, chamadas de self-closing, não têm fechamento.

https://devlife.insper-comp.com.br/aulas/design/introducao-ao-html/introducao/

## Estrutura Básica

Abaixo segue um exemplo de uma estrutura básica de uma página HTML:
```
<!DOCTYPE html>
<html lang="pt-BR">
    <head>
        <title>Exemplo</title>
        <meta charset="UTF-8">
    </head>
    <body>
        ...

        <!-- https://www.tudogostoso.com.br/receita/23-bolo-de-cenoura.html -->
    </body>
</html>
```
Vamos explorar cada elemento desta estrutura:

## !DOCTYPE
A tag !DOCTYPE é especial por ser a única que não representa um elemento.

Essa tag declara a versão do HTML na qual o código está escrito. Antigamente ela era mais complexa, mas hoje em dia precisamos apenas escrever !DOCTYPE html para declarar que o código foi escrito em HTML 5.

## Elemento html
O elemento html representa... tudo! Ou seja, o documento inteiro. Repare que, exceto pela !DOCTYPE (que não representa elemento), todas as tags estão dentro dele.

Esse elemento deve ter um atributo lang que declara o idioma no qual o documento está escrito. Nesse caso, o valor é pt-BR para indicar que esse idioma é o português do Brasil.

## Elemento head
O elemento head representa metadados, ou seja, informações que são sobre o documento mas não fazem parte do documento propriamente dito.

Um bom exemplo de metadado é o primeiro filho, o elemento title. Esse elemento declara qual é o texto que deve aparecer na aba do navegador.

Outro exemplo é o segundo filho, que declara a codificação na qual o documento está escrito. Nesse caso, o valor é UTF-8. Não vamos nos aprofundar nos detalhes técnicos porque eles estão fora do escopo desta disciplina, mas por enquanto basta saber que essa tag (que, aliás, é outro exemplo de self-closing) evita que o navegador tenha problemas com caracteres acentuados.

## Elemento body
O elemento representa dados, ou seja, informações que fazem parte do documento propriamente dito. É por isso que o exemplo anterior está dentro desse.

Na verdade, o que escrevemos além do exemplo anterior nem era necessário, mas...

## Comentários em HTML
...aproveitamos a oportunidade para mostrar como adicionar comentários a um código HTML. Tudo o que você escreve entre <!-- e --> é ignorado pelo navegador.

Lembra do primeiro exercício da primeira parte do handout? A resposta do exercício estava em um comentário no HTML e por isso não aparecia na página mostrada pelo navegador.

## A Estrutura básica
Resumindo: em qualquer código HTML que você escrever, deve incluir no mínimo o conjunto de tags abaixo.

```
<!DOCTYPE html>
<html lang="pt-BR">
    <head>
        <title></title>
        <meta charset="UTF-8">
    </head>
    <body>
    </body>
</html>

```
Vamos chamar esse conjunto de estrutura básica.

## Trabalhando dentro do HTML

Ok, agora que temos noção da estrutura básica de um documento HTML, vamos entender como adicionar mais elementos dentro do mesmo, além de um texto puro.

A seguir iremos passar por algumas das tags mais comuns em uma página.

## Tag de título ``<h1>-<h6>``

Os elementos HTML `` <h1> ``até`` <h6> `` representam seis níveis de título de seção. ``<h1>`` é o nível de seção mais alto e ``<h6>`` é o mais baixo.

Copie o exemplo abaixo dentro do ``<body>`` para testar

```
<h1>título 1</h1>
<h2>título 2</h2>
<h3>título 3</h3>
<h4>título 4</h4>
<h5>título 5</h5>
<h6>título 6</h6>

```

## Tag de texto ``<hr>/<p>``

O elemento HTML ``<hr>`` representa uma quebra temática entre elementos de nível de parágrafo (por exemplo , uma mudança da cena de uma história, ou uma mudança de tema com uma seção). Nas versões anteriores do HTML, representava uma linha horizontal. Pode continuar sendo exibida como uma linha horizontal nos navegadores, mas agora está definida em termos semânticos, em vez de termos de apresentação.

já a tag ``<p>`` define um parágrafo. Navegadores automaticamente adicionam uma linha em branco antes e depois de cada tag ``<p>``

```
<p>
  Este é o primeiro parágrafo do texto. Este é o primeiro parágrafo do texto.
  Este é o primeiro parágrafo do texto. Este é o primeiro parágrafo do texto.
</p>

<hr />

<p>
  Este é o segundo parágrafo do texto. Este é o segundo parágrafo do texto. Este
  é o segundo parágrafo do texto. Este é o segundo parágrafo do texto.
</p>

```

Copie o código acima para ver o resultado.

## Tag de link ``<a>``

A tag ``<a>`` define um *hyperlink*, utilizado para levar o usuário de uma página para outra.

dentro da tag ``<a>``, temos como mais importante o elemento ``href``, que indica o destino do link criado dentro da tag.

Como padrão, links terão as seguintes características nos navegadores:

 - um link não visitado será sublinhado e azul;
 - um link visitado será sublinhado e roxo;
 - um link ativo será sublinhado e vermelho;

Teste o link abaixo:

```
<a href="instagram.com">
```

# CSS: Introdução

## Introdução

## Anatomia

## Seletores

## Inspeção

## Display

## Tamanho

## Posição

## Responsividade

## DESAFIO

