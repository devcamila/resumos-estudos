**_CONCEITOS_**  
Cascading Style Sheets.  
Estilização de páginas HTML.  
Estilo em cascata, CSS sempre pega o **ÚLTIMO** valor atribuído.

---

**_Adicionando CSS ao HTML_**

1. Atributo dentro da tag do elemento HTML.(propriedades separadas com ;)  
   `<p style="color:red">Teste</p>`
2. Elemento `<style></style>` dentro do HTML.
3. Carregando um arquivo css usando `<link rel="stylesheet" href="style.css">`

Ordem de aplicação do CSS será sempre **Arquivo(css)** -> **Elemento(`<style></style>`)** -> **Propriedade(inline)**.  
Style inline tem prioridade, usar com cuidado!  
Para renderizar o css antes do conteúdo:  
`<style></style>` costuma aparecer na primeira linha do `<body></body>` ou, mais comumente, na última linha do `<head></head>`.

---

**_SELETORES_**  
_Encapsulamento_

Seletor é elemnto hmtl que será alerado.  
Pode ser uma tag, uma classe ou um id.
**tag**: body {}, div{}  
**classe**: .titulo {}, .cabecalho{}  
**id**: #titulo, #cabecalho{}

    `seletor {
        propriedade: valor;
    }

exemplo:

    body {
        background-color: red;
    }

    .class li a {}: vai seguir esse caminho;  
    .class, li , a {}: vai alterar todos esses três seletores do documento;  
    .class > p {}: altera filhos diretos;  
    .class:first-child {}: altera a primeira tag filha.  
    .class:first-letter {}: altera a primeira letra do elemento.  
    .class:first-child {}: altera a primeira linha do elemento.  
    .class:last-child {}: altera a última tag filha.  
    * {} : Todos os elementos.  

---

**_BASICOS_**

    background-color: cor de fundo
    color: cor fonte ou elemento
        rgba(0,0,0,0.3): útimo número(0.3) é a transparência da cor, vai de 0 a 1.  
    background-image: imagem de fundo
    background-position: posição do imagem de fundo;
    background-repeat: se a imagem será repetida;
    background-size: tamanho imagem de fundo;


    width: largura
    height: altura

---
    padding: espaço interno ao elemento
    margin: espaço ao redor do elemnto

        margin : 10px = Todos os lados com margem 10px  
        margin : 10px 5px = Margem de 10px no topo e embaixo e de 5px dos lados  
        margin : 1px 2px 3px 4px = Topo 1px, direita 2px, baixo 3px e esquerda 4px. Lados determinados em sentido horário (top, right, bottom, left);  

    margin-top: topo  
    margin-right: direita  
    margin-bottom: baixo  
    margin-left: esquerda  

        padding : 10px = Todos os lados com margem 10px  
        padding : 10px 5px = Margem de 10px no topo e embaixo e de 5px dos lados  
        padding : 1px 2px 3px 4px = Topo 1px, direita 2px, baixo 3px e esquerda 4px. Lados determinados em sentido horário (top, right, bottom, left);  
        
    padding-top: topo  
    padding-right: direita  
    padding-bottom: embaixo  
    padding-left: esquerda  

---
    border: borda (ex:  border: 3px solid black)
    valores para line-style: none, hidden, dotted, dashed, solid, double, groove, ridge, inset, outset.
    border-radius: arredonda as bordas. Se colocar 50%, transforma em um circulo
    box-shadow: sombra da caixa.

    text-align: alinhamento do texto.
    text-decoration: none(nenhum), sublinhado, e outros.  
    list-style: defina decoração que terá no inicio da lista.  

**dica: coloque background-color no elemento para entender melhor padding e margin.**

---
**\*FONTS**

    font-family: Nome da fonte
    font-size: Tamnho
    font-weight: Peso (negrito)
    font-style: oblique, italic
    line-height: altura da linha, font

     @import url(); importa uma font para o documento. => use o site (https://fonts.google.com/) para pegar fontes

---

**_LINKS_**
    :link : não visitado
    :visited : visitado
    :hover : passar o mouse
    :active : clicar

    :focus : durante o foco
    transition: ms

**_DISPLAY_**
    block: ocupa a linha inteira; 
    inline: ocupa só o espaço da caixa;
    flex: layout reponsivo em blocos;  
    flex-direction: row(linha) e column(colun);  
    justify-content: alinhamento horizontal do elementos;  
    align-center: alinhamento vertical do elementos;  
    grid: layout reponsivo manipulado como uma matriz;  

    !important:** forçar um estilo

---
**_RESPONSIVIDADE_**
- evitar repetir código
- evitar estilo inline (são absolutos)
- use grids e flexbox
- evite estilos absolutos e relativos
- use media querys

**_Media queries_**
    @media (max-width: ){

        Altera os seletores de acordo com o tamanho estipulado.

    }

Tem outras propriedades como and que acrescentam condições.

**Extensão que redimensiona para várias resoluções de tela:** https://chrome.google.com/webstore/detail/window-resizer/kkelicaakdanhinjdeammmilcgefonfh

---

**_Indo Além_**  
https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element  
https://developer.mozilla.org/pt-BR/docs/Web/CSS
https://devdocs.io/  
https://css-tricks.com/almanac/properties/a/align-items/  
Grid: https://cssgridgarden.com/  
Flexbox: https://flexboxfroggy.com/  
 https://mastery.games/flexboxzombies/  
 https://flukeout.github.io/

---
