***JAVASCRPIT***  
É uma linguagem multi paradigma:  
-Procedural  
-POO
-Funcional  

***COMENTÁRIOS***<br>
*ATALHO: seleciona e ctrl + ;*<br>
JavaScript: //: uma linha ou /**/:  várias linhas<br>
html (<!--     hífen->) <br>
css /* */

---
***VARIÁVEIS E TIPOS PRIMITIVOS***<br>
- **Identificadores(nomeVariavel):** começa com letra, $ ou _
- Sempre usar espaço entre operadores e após a virgula
- **Indentação:** use dois espaços
- Sempre termine uma insttrução simples com ;
- Tipos de variáveis= string, number, boolean, null, undefined, symbol

**var:** escopo global, escopo de função, pode ser redefinida e sofre hosting<br>
**let:** escopo de função, escopo de bloco, pode ser redefinida<br>
**const:** escopo de função, escopo de bloco, não pode ser redefinida<br>

**null(vazio) !== undefinded(indefinido)**<br>

**Concatenar:** Juntar variáveis. <br>

    var nome = 'Camila '
    var sobrenome = 'Lacerda'
    var nomeCompleto = nome + sobrenome


**Template Strings:**<br>
Possível interpolar strings e expressões.<br>
Além de criar strings multi-linhas.<br>

    `Olá ${nome}!`

    Space holder: ${}

---
***PRECEDÊNCIA DE OPERAÇÕES***   
parênteses: ()    
pontenciação: **   
multiplicação e divisão: * / %   
soma e subtração: + -   
resto: % : mode   

---
***DECLARAÇÕES E EXPRESSÕES***   
* **Expressões** produzem valores e podem ser escritos onde um valor é esperado. Exemplo: Como argumento de uma função.    
* **Declarações** performam ações. Exemplo: laços e condicionais.  

---
***CONDICIONAIS***   
**IF / ELSE**

    if (condição) {
        ação ;
    } else if (condição) {
        ação ;
    } else {
        ação ;
    }

***SWITCH***

    switch (condição) {
        case 'A' :
            ação ;
                break;
        case 'B' :
            ação ;
                break;
        case 'C' :
            ação ;
                break;
        default :
            ação;
    }

***OPERADOR TERNÁRIO*** 

    (condição) ? ação : outra ação

---
***OPERAÇÕES CLASSE MATH***   
**Math.abs(num**): Retorna o módulo, ou valor absoluto, de um número.  

*Arredondamentos*   
**Math.ceil(num):** Retorna o menor inteiro que é maior ou igual a um número.  
**Math.floor(num):** Retorna o maior inteiro que é menor ou igual a um número.  
**Math.round(num):** Retorna o valor arrendondado, para o valor inteiro mais próximo.  
*Valores máximos e mínimos*  
**Math.max(num1, ..., numN):** Retorna o maior dentre os parâmetros recebidos.  
**Math.min(num1, ..., numN):** Retorna o menor dentre os parâmetros recebidos.   
*Potência e Raiz*
**Math.pow(base,exp):** Retorna a base elevada à potência do expoente.  
**Math.sqrt(num):** Retorna a raiz quadrada positiva de um número.  
*Geração de números pseudo-aleatórios*
**Math.random():** Retorna um número pseudo-aleatório entre 0 e 1.  
*Funções trigonométricas e PI*  
**Math.PI** Contém o valor aproximado do PI.  
**Math.sin(num):** Retorna o seno de um número. 
**Math.cos(num):** Retorna o coseno de um número.  
**Math.tan(num):** Retorna a tangente de um número.  

----
***OPERADORES LÓGICOS***  
==	igual  
!=	diferente  
<	menor  
<=	menor igual  
>	maior  
>=	maior igual  
&& e  
|| ou   
!	não ou negação  
=== e !== estritamente igual e estritamente diferente  

---
***TRUTHY E FALSY***
Normalmente em uma linguagem apenas variáveis booleanas ou operadores / funções que produzem um booleano.No entanto, javascript é um pouco mais permissivo.  
Ele tem valores que são interpretados como true e false, quando são usados como booleanos.  
**Falsy**: 0, undefined, null, NaN, "", ''  
**Truthy**: demais.  