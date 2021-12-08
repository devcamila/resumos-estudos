***Iniciando Projeto***

    npm install -g @angular/cli (instalar angular)

    ng new my-first-app (iniciar novo projeto)

    cd my-first-app (abrir pasta projeto)

    ng serve (rodar projeto)

---
***Instalat Bootstrap***

    npm install --save bootstrap@3

    importar no styles do arquivo style principal


---
***Criando Componente***

**Manualmente**
    @Component({
        selector: 'app-nome-componente',
        templateUrl: 'endereço html do componente',
        styleUrls: ['endereço css do componente']
    })

    exports class nome-componenteComponent {

    }

**Pelo Terminal**

    ng generate component <nome>
    ng g c nome-componente

**Declarar no *AppModule***
Dentro do declarations, colocar o nome do componente.  
Ele importa automaticamente.  
