***Web Front-End Estática***

**Html**   
Estrutura e conteúdo  
(substantivos)  

**Css**  
Estilização  
(adjetivos)  

**Javascript**  
Define comportamentos  
(verbos)  

---
***Teoria HTML***  
HTML significa Hyper Text Markup Language.  
Linguagem de marcação 

**Conceitos**  
***ELEMENTOS***: São representados pelas tags. Exemplo: botão, parágrafo, imagem, lista, tabela.  

    <button>
    <p>
    <table>
***CONTEÚDO***: Informação que está entre uma tag de abertura e uma tag de fechamento. Exemplo: 

    <p> ... </p>

***ATRIBUTOs***: São pares chave-valor, separados por = e os valores devem estar envoltos em aspas.  
Exemplo: width="200px", src="http://..."

**Abertura e fechamento**  
As tags podem necessitar de fechamento.  
Exemplo: 

    <p>
    Lorem Ipsum é um texto modelo da indústria tipográfica e de impressão. O Lorem Ipsum tem vindo a ser o texto padrão usado por estas indústrias desde o ano de 1500.
    </p>

    <button>Enviar</button>

ou as que se fecham sozinhas (self-closing)  

    <img>
       
    <input>

**Comentar código**: ctrl + ;   
ou < !--  --> (ignorar espaço)

---
***Estrutura***
Deve começar pela tag **html** e deve ter um **head** e um **body**.  

***!DOCTYPE html***: indica que estamos estamos usando a versão 5 do HTML. 

***HEAD*** contém os metadados da página como título, autor, charset, etc. Também podemos linkar arquivos CSS, fontes e favicon.  

***BODY***: conteúdo visível da página.  

***LANG***: indica ao navegador qual é o *idioma do conteúdo*, com isso ele é capaz de oferecer opções de tradução ou orientar leitores de tela (para deficientes visuais) de qual voz e idioma deve ser usado.
Exemplo:

    <html lang="pt-br">

***TITLE***: título da página que será mostrado na aba do navegador.

***meta charset='UTF-8'***: encoding é utilizado pela página.

**Atalho**: digite **!** ou **html5** para que o vscode carregue essa estrutura básica.  

    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
    </head>
    <body>
        
    </body>
    </html>

---
***ELEMENTOS SEMÂNTICOS***  
Comportam-se como divs na página, mas eles tem significado.  

**Os principais são**:  
**main**: conteúdo principal do documento.  
**section**: uma subdivisão do documento dentro do main.  
**article**: um conteúdo independente, como o post de um blog.  
**aside**: conteúdo "lateral" como menus ou área de anúncios (ads) em um blog/site.  
**header**: uma área, geralmente acima do conteúdo main, onde situa-se comumente a navegação.  
**footer**: rodapé, geralmente apresenta um mapa do site.  
**nav**: um componente de navegação com links ou botões para as diversas páginas.  
**figure**: um pequeno conteúdo a parte do todo, como uma imagem ou vídeo. Pode usar figcaption como legenda.  
**template**: um conteúdo HTML que será utilizado por javascript. Ele por padrão não aparece na página.

---
***Divisões de texto***:  

**div**: divisão do espaço da tela, não tem aparência;  
**span**: divide uma parte de um texto permitindo estilizá-la;  
**p**: parágrafo;  
**pre**: texto pré-formatado (respeita espaços em branco e quebras de linha);  

---
***Formatação de texto***:  

**b ou strong**: negrito; //prioridade a tags strong e em, são mais semânticas.  
**i ou em**: itálico;  
**u**: sublinhado;  
**sub**: texto subscrito;  
**sup**: texto superscrito;  
**h1**: títulos - vai do H1 ao H6, o tamanho diminui conforme o número aumenta. O H1 é o mais importante e o H6 o menos. Seguir essa hierarquia melhora o SEO da página.  
**br**: quebra de linha;  
**font**: define atributos de fonte, como, color, family e size.

---
***Referências***:  

**a**: link;  
**img**: imagem  

*atributos*  
**src=""**: busca a imagem  
**alt**: legenda para caso a imagem não carregue. Importante para SEO e para os leitores de tela de deficiêntes visuais.  
**href=""**: endereço do link  
**target="_blank"**: abre link em nova guia


---
***Listas***:  

**ol**: lista enumerada (ordenada);  
**ul**: lista não-ordenada;  
**li**: item de lista;  

---
***Tabelas***:  

**table**: tabela;  
**thead**: cabeçalho de tabela;  
**tbody**: corpo de tabela;  
**tfoot**: rodapé de tabela;  
**tr**: linha de tabela;  
**th**: célula de cabeçalho;  
**td**: célula de dados;  

---
***Formulários***:  

**form**: formulário;  
**input type='text'**: campo de texto (uma linha);  
**input type='checkbox'**: checkbox;  
**input type='radio'**: radio;  
**input type='button'**: botão;  
**button**: botão;  
**textarea**: campo de texto de múltiplas linhas;  
**select**: caixa de seleção; 
**option**: item dentro da caixa de seleção;  
**fieldset**: agrupa elementos do formulário;
**legend**: legenda para o grupo fieldset;
**label**: rótulo do elemento de formulário;

*atributos* 
**name**: a partir dele que o servidor poderá compor as informações em pares chave-valor, chave=name e valor=value. Os radios devem ter o mesmo name. No select o name será atributo dele e os value atributos de option;  
**value**: valor do input;   
**type**: tipo do input ou arquivo;  
**action**:  URL do servidor;  
**method**: método http usado, sempre use post;  
**for**: especifíca qual elemento a label está ligada;  

---
***Midia***  
**audio**: arquivo de aúdio;  
**video** : arquivo de vídeo;  

*atributos*   
**controls**: criar controle de aúdio;  
**autoplay**: começa a tocar automaticamente;  
**loop**: tocará em loop;  
**muted**: carrega mutado.
**preload**: define quando o arquivo será carregado(*auto, metadata, none*);
**type**: "audio/ogg", audio/mpeg, video/mp4"  
**height**: altura do vídeo;  
**width**: largura do vídeo
**poster**: imagem que aparecetá até seu carregamento ou até usuário clicar no play.

---
***Indo Além***  
https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element  
https://www.w3schools.com/html/  
https://devdocs.io/  
