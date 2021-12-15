***Semântica e Acessibilidade***      
Porque usar com tags semânticas (h1, nav) e não apenas com tags genéricas (div, span) ?

* Acessibilidade: Leitores de tela (JAWS, NVDA, VoiceOver)
* Browsers e funcionalidades: Estilo padrão e organização
* reconhecimento de informações para a indexação por robôs de busca (SEO)


**ACESSIBILIDADE**  
A **navegação pelos cabeçalhos** é um dos principais métodos utilizados para procurar conteúdo na página.   
Os p**ontos de referência (landmarks)** das páginas são utilizadas por mais de 75% dos usuários para navegar pelo conteúdo.   

***Atributos:***  
**aria-label**: Título da região visualmente escondido, mas lido pelo leitor de tela.
**aria-labelledby**: Caso o título exista na tela, marque o mesmo com um id e use este atributo para criar uma relação entre eles. Evita repetição desnecessária.

    <article aria-labelledby="celtitulo">
      <h2 id="celtitulo">Celulares</h2>
      <p>Conheça mais as marcas que vendemos no site</p>
    </article>


***Listas***    
Listas são anunciadas pelo leitor de tela e o usuário é informado previamente quantos itens existem na lista. 
 ***O ideal, visando acessibilidade, é o uso de listas dentro da tag nav***