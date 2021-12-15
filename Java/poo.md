***Fundamentos da Orientação a Objetos***   
Alan Kay foi o pai da POO.  

***UML**    
***Diagrama de Classes***   

Nome da classe sempre começa em maiúsculo.  
Atributos em minúsculo.   
Métodos em minúsculo seguidos de parênteses. 

    public class Caneta {
      String modelo;
      String cor;
      float ponta;
      int carga;
      boolean tampada;

      void status() {}
      void tampar() {}
    }

**O que é uma classe?**   
Define atributos e métodos que serão compartilhados por um objeto.  

**O que é objeto?**  
Coisa concreta ou abstrata que seja percebida pelos sentidos e descrita por meio de:
* Características (Atributos, propriedades);
* Comportamento (Métodos, procedimentos, rotinas internas);
* Estado (Características atuais);

Todo objeto é criado a partir de uma classe (um molde).

**Instanciar**  
Gerar um objeto a partir de uma classe.   
Usamos a palavra new.

*Abstração*   
Quais atributos são relevantes na minha classe.   

*This*    
É uma referência ao objeto que chamou. 

---
***Modificadores de Visibilidade***   
Indicam o nível de acesso ao componentes internos da classe.   

**Padrão(default)**: padrão de pacote;
**+** = público (public);    
A classe atual e todas as outras classes.   
**-** = privado (private);    
Somente a classe atual.   
**#** = protegido (protected);    
A classe atual e todas **suas** sub-classes.  

***Quando o método main está dentro de uma classe que está ultilizando uma classe com atributos e métodos protegidos. O método main tem acesso a eles.**

    public class Aula02 {
    public static void main(String[] args) {
        Caneta c1 = new Caneta();
      }
    }

---
***Métodos Acessores***
**Getters**: Garante acesso a algum dado do objeto, sem dar acesso a todo objeto.
   
Ao invés de:
    saldo = conta01.saldo;
   
Usamos: 
    saldo = conta01.getSaldo();
    
***Métodos Modificadores***
**Setters**: permite a mudamça de algum dado do objeto, sem dar acesso de mudar todo objeto.
   
Ao invés de:
    conta01.saldo += 100;

Usamos: 
   conta01.setSaldo(100);

***Método construtor***    
**Construct**: Determina que ações devem ser executadas quando se cria um objeto.

---
***Encapsulamento***      
*Encapsular não é obrigatório mas é uma boa prática.*
Ocultar partes indepedentes da implementação, permitindo a existência de uma parte desconhecida para o mundo exterior.

*Um objeto encapsulado deve possuir uma interface bem definida!*    
**Interface**: É o intermédio do objeto com o mundo exterior. Define o que pode ser feito no componente.       
Interface não tem atributos, **apenas métodos.** 
Métodos abstratos, é previsto mas não é implementado.   
A interface é criada antes da classe.   