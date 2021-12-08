***Geral***  
**block**: ocupa a linha inteira, box model. (h1, p, div)
**inline:** ocupa só o espaço da caixa e tem valores padrões;  
**inline-block:** continua inline mas recebendo propriedades do box model.  
**none:** remove o elemento.  


*Alinhamento do container* (só funcionam se houver espaço)    
**align-content:** alinhamento vertical do elementos;   
**justify-content:** alinhamento horizontal do elementos;   
**place-content:** atalho que une align e justify;  
  
*Alinhamento dos itens*  
**align-items:** alinhamento vertical do elementos;  
**justify-items:** alinhamento horizontal do elementos;  
**place-items:** atalho que une align e justify;  
  
*Alinhamento de um único iten*  
**align-self:** alinhamento vertical do elementos;  
**justify-self:** alinhamento horizontal do elementos;  
**place-self:** atalho que une align e justify;  

---
***DISPLAY GRID***    
*Grid Container*
**display:** grid;  
**grid-template-columns:** 1fr 3fr; ( entro com o tamanho de cada coluna);  
**grid-template-rows:** 1fr 3fr; ( entro com o tamanho de cada linha);  
**gap:** espaçamento entre os elementos;  
**fr:** é uma unidade fracionária que terá como objetivo distribuir o espaço restante, entre os elementos do grid.  
**grid-area**: união do grid column e grid row;  

**Grid Item**  
*grid-column:* quais colunas serão ocupadas pelo grid item.  
**grid-column:** 3; (ocupará a coluna 3)  
**grid-column:** 1/3; (ocupará da coluna 1 até a 3)   
**grid-column:** 1/-1; (ocupará da coluna 1 até a última columa)   

**grid-column-start:** 2 (começa na coluna 2)   
**grid-column-end:** 4 (termina na coluna 4)    
**grid-column:** span 2 (ocupar duas colunas a partir de onde ele estiver.)   

*grid-row:* quais colunas serão ocupadas pelo grid item.  
**grid-row:** 3; (ocupará a coluna 3)  
**grid-row:** 1/3; (ocupará da coluna 1 até a 3)   
**grid-row:** 1/ -1; (ocupará da coluna 1 até a última linha)   

**grid-row-start:** 2 (começa na coluna 2)   
**grid-row-end:** 4 (termina na coluna 4)    
**grid-row:** span 2 (ocupar duas colunas a partir de onde ele estiver.)   

---
***DISPLAY FLEXBOX***
**display:** flex (Os filhos passam a ter um tamanho flexível e ficam um ao lado do outro.)   
**flex-wrap:** wrap (Caso não caiba todos os elementos em uma mesma linha, quebre para a próxima.)    
**gap:** (espaçamento entre os elementos)  

***No item***
**flex-grow:** 1 (Se esse elemento deve crescer para ocupar o espaço vazio. O 0 impede o crescimento, valores maiores que 0 funcionam como a unidade fr do css grid.)  
**flex-basis:** 200px (Valor inicial antes de distribuir o espaço em branco.)     
**flex-shrink:** 0 (Caso exista um valor de base, o flex-shrink irá determinar se esse valor pode ser reduzido ou não. 0 significa que ele não pode ser reduzido.)
**flex:** 1 (Atalho para flex-grow: 1; flex-shrink: 1; e flex-basis: 0)


***POSITION***    
A propriedade position possui valores que remove o elemento do fluxo padrão do documento. O padrão é o valor static.    
**position:** fixed (Fixa o elemento na tela.)    
**position:** relative (Mantem o elemnto no fluxo mas nos permite manipularmos e continua ocupando o espaço anterior)    
**position:** absolute (Relativo ao elemento pai e deixa de ocupar o espaço anterior. *É preciso atribuir ao elemento pai o position relative*)         
**top, right, left, bottom** (Define o posicionamento dos elementos que não estão no fluxo padrão e só funcionam se mudardos o position.)
**z-index:** índice de profundidade. (Só funcionam se mudardos o position e ao mudarmos ele assume o index maior, seguido da ordem no hmtl)