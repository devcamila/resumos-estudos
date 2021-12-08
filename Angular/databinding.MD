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
**Pai para filho (Input)** filho pega  
Filho está recebendo do componente pai.  


*ts pai:*

     frase: string ="eu sou seu pai" (CRIO UM DADO)


*html pai:*

    <app-filho [paiFrase]='frase' ></app-filho> (CHAMO A TAG FILHO FAZENDO UM BIND, atribuindo a váriavel do filho aos dados do pai)


*ts filho:* 
    export class FilhoComponent {
         @Input() paiFrase!:string (CRIO UMA VARIAVEL QUE IRA RECEBER OS DADOS)
    }

*html filho:* 

    <p>{{paiFrase}}</p> (CHAMO OS DADOS PELA VARIAVEL QUE CRIEI)

*para acessar com outro nome:* 
    @Input('fireElement') element: string;
    será chamado por fireElement


---
**Filho para pai (Output)** filho manda por meio de eventos

*html child:*

    <button (click)="onClick"> Emitir Evento </button>

    (Crio um botão que chamará a função e emitirá o evento)

*ts. child:*

    fraseFilho: string = 'Eu sou seu filho' (CRIO O DADO)

    @Output() nomeEvento = new EventEmitter<TIPO_DE_DADO>(); (CRIO O EVENTO)

    onclick(){
        this.nomeEvento.emit(this.fraseFilho); (CRIO A FUNÇÃO QUE APARTIR DO EVENTO VAI EMITIR O DADO)
    }

*html pai:*

    <app-filho (clickEvt)="onClickEvt($event)"></app-filho> 

    (CHAMANDO O EVENTO clickEvt ELE EXECUTARÁ A FUNÇÃO onClickEvt E RECEBERÁ OS DADOS EMITIDOS PELO COMPONENTE FILHO ATRAVES DO $event.

*ts. pai:*

     pegarFraseFilho: any; (CRIO VARIÁVEL PARA GUARDAR ESSE DADO)

     onClickEvt(pegarFraseFilho: any) {
      this.pegarFraseFilho = pegarFraseFilho
     }

     (FUNÇÃO QUE RECEBERÁ ESSE DADO)

---
***Referências locais em Templates***
