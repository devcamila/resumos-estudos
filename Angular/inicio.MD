***Iniciando Projeto***

    npm install -g @angular/cli

    ng new my-first-app

    cd my-first-app

    ng serve

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
