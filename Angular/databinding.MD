***Conceito***  
Databinding significa comunicação. Comunicação entre o template (html) e o código TypeScript (lógica de negócio).  
  

Dados fluindo do typescript => Html : podemos utilizar interpolação de string ou property binding (binding de propriedade)..  

Dados fluindo do Html => typescript :Event Binding (Binding de Eventos).

Dados fluindo nos dois sentidos: two-way-binding.

--- 
**Interpolação de string**  
Qualquer valor no componente que se resolva como uma string pode ser exibido utilizando interpolação de string, até uma função, caso ela retorne um string. 

    {{ string }}

---
**Property Binding (Binding de Propriedade)**   
Para modificar dinamicamente o valor de uma propriedade.

    <button [disabled]="!canShowButton"></button>

---
**Event Binding (Binding de Evento)**
Podemos escutar os eventos e ao escutar determinado evento, executar algum tipo de ação.  

    <button (click)="onClickButton()"></button>

Quando queremos ter acesso no nosso código typescript aos dados emitidos com determinado evento utilizamos **$event**.

---
**Two-Way-Binding**  
Trabalha nos dois fluxos.

    <input type="text"
    [(ngModel)]="randomText"

---
**Pai para filho (Input)**
Filho está recebendo do componente pai.  

*html pai:*

    <app-child-component [element]="myElement"></app-child-component>


*ts:* 
    export class AppChildComponent {
         @Input() element: string;
    }

*para acessar com outro nome:* 
    @Input('fireElement') element: string;
    será chamado por fireElement


---
**Filho para pai (Output)**

*ts. child:*
    @Output() elementCreated = new EventEmitter<{elementName: string}>();

Dessa forma estamos criando um evento como outro qualquer, como o evento click por exemplo, porém customizado e nomeado de elementCreated. Esse evento irá emitir com ele um objeto com o nome do elemento.  

    onCreateElement() {
        this.elementCreated.emit();
    }

A função onCreateElement será chamada toda vez que um elemento for criado no componente filho, e ao ser chamada, o evento elementCreated será emitido para os componentes pais.  

*html pai:*

    <app-child-component (elementCreated)="onElementCreated($event)"></app-child-component>

Agora, toda vez que o evento elementCreated ocorrer no componente filho, a função onElementCreated do componente pai será executada, recebendo os dados emitidos pelo componente filho através do **$event**.

*para acessar com outro nome:*
    @Output('elmCreated') elementCreated: string;
    o evento será elmCreated


***Referências locais em Templates***
