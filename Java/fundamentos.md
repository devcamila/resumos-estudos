***Introdução ao Java***  
  
* Orientada a objetos.
* Criada pela Sun Microsystems em 1995.
* Comprada pela Oracles.
* mantida pela JCP (Java Community Press) que organiza as discussões e mudanças através de JSR (Java Specification Requests).

***Tipos Primitivos***
Java é uma liguagem fortemente tipada.   
Existe oito tipos, chamados primitivos: 
Primitivos guardam apenas um valor.     
Não pode ser null.      

* 4 para números inteiros
* 2 para números de ponto flutuante
* 1 para caracteres (em esquema Unicode)
* 1 para valores lógicos de verdadeiro ou falso.

**Tipo inteiro**  
* byte (1 byte): -128 a 127
* short (2 bytes): -32.768 a 32.767
* int (4 bytes): -2.147.483.648 a 2.147.483.647
* long (8 bytes): -9.223.372.036.854.775.808 a 9.223.372.036.854.775.807

Os tipos **byte e short** costumam ser utilizados em algoritmos com muitos números pequenos e necessidade de desempenho.    
O tipo **long** sempre vem acompanhando do sufixo L, por exemplo, a quantidade de habitantes do planeta seria representada pelo long 7_800_000_000L.


**Tipo de ponto flutuante**   
* float (4 bytes): aprox. +- 3.40282347E+38F (6-7 dígitos decimais significativos)
* double (8 bytes): aprox. +- 1.797691313486231570E+308 (15 dígitos decimais significativos)
  
O tipo **double** tem o dobro da precisão do tipo float. Para tipos decimais, esse tipo, geralmente, é a escolha padrão.*Porém, este tipo nunca deve ser usado para representar valores exatos, como moedas. Nesse caso, use BigDecimal.*

**Assim como o tipo long necessita do sufixo L, da mesma forma float necessita de F e double necessita de D.**

---
***Tipos por referência (não primitivos***
Não-primitivos guardam além do valor, propriedades e funcionalidades.   
Pode ser null.      
Armazena endereço de memória.

**Tipo Strings**    
Qualquer sequência de caracteres (qualquer Unicode válido) representada entre aspas duplas "" é uma string Java.  

    String s = "this is a string";

Strings são **imutáveis.** Portanto, toda e qualquer manipulação de strings resulta numa nova string.   
    
Assim como String é uma classe, também existem outras classes no pacote **java.lang** que representam os tipos primitivos:*Byte, Integer, Double, Short, Float, Long* para os tipos numéricos; *Char e Boolean* para os demais.   

**Wrapers**
Encapsulam os tipos primitivos em um objeto contendo métodos. Por exemplo, conversão.

**Tipo Enums**   
* enumerations ou enums.   
* valores finitos de uma determinada representação.  
* Por exemplo, dias das semana, fases da lua, meses do ano.
    
    public enum DaysOfWeek {
    MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY, SATURDAY, SUNDAY
} 

**Demais Classes**

  

---
**Variáveis**   
Para declarar primeiro colocamos o tipo e depois o nome da variável.    
O nome deve ser escrito em camelCase.   
Pode ser inicializada (colocado seu valor) na declaração ou após.
Caso seja apenas declarada, o java define valores padrões.    

    boolean done;
    int age = 28;
    long earthPopulation;
    double pi;

    done = true;


**Constantes**
* as constantes representam valores fixos e imutáveis.    
* notação snake case. (letras em maiúsculas e palavras sepradas por _ )   
* o modificador final indica que o valor da constante não pode ser alterado.

    final int QUANTIDADE_TENTATIVAS = 3;


---
***Operadores***
* Aritméticos: soma (+), subtração (-), multiplicação (*) e divisão (/);
* Lógicos: negação (!), E (&&), OU (||) // duplo pipe
* Relacionais: maior que (>), menor que (<), igual (==), diferente (!=)
* Ternário: ? :
*  mod: % resto da divisão

**Precedência**
**postfix**	exp++ exp--
**unary**	++exp --exp +exp -exp ~ !
**multiplicative**	* / &
**additiv**e	+ -
**relational**	< > <= >=
**equality**	== !=
**logical AND**	&&
**logical OR**	||
**ternary**	? :
**assignment**	= += -= *= /= %=


***ARRAYS***
Um array é um contêiner de objetos que armazena uma quantidade **limitada** de elementos de um **único tipo**.      
Seu Tamanho é definido em sua declaração.   
Seus elementos são acessados por um índice, que começa em 0 e até ate seu comprimento(length) - 1. Logo, em um array com 10 posições temos índices de 0 a 9.    


    Um array com 10 posições:

    int[] arrayInteiros = new int[10];
    char[] arrayChar = new char[5]

**String é um array de caracteres**         
Como, char representa um único carácter Unicode, String representa uma sequência de caracteres, ou seja, um array de char.

***Métodos para manipular array***
**Copiar** java.util.Arrays.copyOfRange(ARRAY, INICIO, FIM);        
O fim não é incluido.


***SAÍDAS***
Usando expressões:
    System.out.println(expression);
    System.out.println("Hello World") //Hello World

Usando string:
    String nome = "Dev Camila";
    System.out.println(nome); // Dev Camila

Concatenando: 
    String nome = "Dev Camila";
    System.out.println("Hello, " + nome); // Hello, Dev Camila

**Format String Syntax**
Essa sintaxe permite o uso de *marcadores de argumentos*.   
Cada marcador define uma variável que será substituída pelo valor contido nos *arguments*

**format** = expressão que será escrita em console.
**arguments** = sequencia de valores, separados por vírgulas, correspondente a cada marcador definido no primeiro parâmetro (format).

**Marcadores:**     
   * s: formats strings
   * d: formats decimal integers
   * f: formats the floating-point numbers
   * t: formats date/time values

Usando método printf:

    System.out.printf(format, arguments); 
    String nome = "Dev Camila";
    System.out.printf("Hello, %s", name); // Hello, Dev Camila


***ENTRADAS***      
**String[] args**:
A forma mais simples de ler entradas do usuário do programa é através do array args contido na assinatura do método main.
O array args é preenchido quando nosso programa é inicializado.     
Podemos definir valores, separados por virgula, como argumentos.
Serve em cenários simples.      

Para definir:

    System.out.printf("Hello, %s.", args[0]);

Executamos no terminal:

    java caminho-da-aplicação.NomeDaClasse VALOR DO INPUT
    java br.com.letscode.java.Saudacao "Dev Camila"

Porém, o array args é do tipo string, para tratar números é necessário converter.
    
Para converter:
    tipo nomeVar = Tipo.parseInt(STRING);

    int numero = Integer.parseInt(args[0]); 
    System.out.printf("Você informou o número %d.", numero);

**java.util.Scanner**   
        Scanner sc = new Scanner(System.in); //Declarou o tipo Scanner
        System.out.println("Informe o peso da primeira pessoa em kg"); //Instrução
        double peso1 = sc.nextDouble(); //Aqui ele recebe e guarda na var peso um como double
Como esperamos um valor do tipo double, usamos a funcionalidade nextDouble.



----
1- Logica da programação
2- Algoritmo ( Passo a passo, loopings, ifs e etc. )
3-  Abstração
4- Estrutura de dados
5- Linguagem de tua escolha