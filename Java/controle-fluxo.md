***Estruturas Condicionais***   

**IF**    
Condicional simples.  
Só é executado quando a condição for verdadeira. 

    int number = 1;
    if (number == 1) {
      System.out.println("O número é 1");
    }

**ELSE**
Condicional composto. 
Será executado caso a condição não seja verdeira.   

Podemos usar **else if** para encadear outras condições após o *if*.  

    int number = 1;
    if (number == 1) {
      System.out.println("O número é 1");
    } else {
      System.out.println("O número é diferente de 1");
    }

**SWITCH**
Devemos utilizar quando queremos comparar a mesma variável ou expressão com várias opções.

    int number = 1;
    switch (daysOfWeek) {
      case 1:
      System.out.println("Hoje é Domingo");
      break;
      case 2:
      System.out.println("Hoje é Domingo");
      break;
      default:
      System.out.println("Número inválido");
      break;
    }

***Estruturas de repetição***     

**WHILE**   
Executa continuamente um bloco de código de acordo com uma expressão booleana.     
Enquanto o número for menor que 10 será executado e incrementada +1.  
Quando number for igual a 10, ele sai do laço de repetição.   

    int number = 1;
    while (number < 10) { 
     System.out.println("Número menor de 10");
     number++
    }

**DO-WHILE**    
Enquanto no while o bloco pode não ser executado. No do-while é garantido pelo menos uma repetição, pois, a expressão será analisado após essa execução.

    int number = 1;
      do {
        System.out.println("Número menor de 10");
        number++;
    } while (number < 10);

**FOR**
Ideal para percorrer um conjunto definido de valores.   
    for (int i = 0; i < 10; i++) {
      System.out.println("Número menor de 10");
    }

***Obs***: É comum o uso de variáveis i, j, k como variáveis de controle do laço for.   

**FOREACH**
O próprio compilador Java entende que estamos percorrendo um array, e associa cada valor contido no array à variável informada (item). 

    int[] numbers = {1,2,3,4,5,6,7,8,9,10};
      for (int item : numbers) {
        System.out.println("Number is: " + item);
    }


---

***MATRIZES***
Um array é um contêiner de dados que armazena uma quantidade limitada de elementos de um único tipo.    
No entanto, se um array é um tipo, então podemos declarar "arrays de arrays".   
Matrizes são arrays de arrays.    
    
Para criamos uma matriz (ou array bi-dimensional) de 3 linhas e 3 colunas. A sintaxe será a seguinte:
A primeira notação de colchetes representa as linhas e a segunda as colunas.    
Para referenciar cada elemento matriz devemos passar as duas posições. 

    int[][] matrizInteiros = new int[3][3];
    int[][] matrizInteiros = {{1,2,3},{4,5,6},{7,8,9}};

    System.out.println(matrizInteiros[0][0]); // será impresso 1
    System.out.println(matrizInteiros[2][3]); // será impresso 6

**Laços aninhados**
Para percorrer cada uma das posições da nossa matriz, precisaremos aninhar laços.   
Para uma matriz (2D) precisaremos de 2 laços; para uma matriz 3D, 3 laços; e assim por diante.

    int[][] matrizInteiros = {{1,2,3},{4,5,6},{7,8,9}};
      for (int i=0; i < matrizInteiros.length; i++) {
        for (int j=0; j < matrizInteiros[i].length; j++) {
          System.out.println(matrizInteiros[i][j]);
        }
    }