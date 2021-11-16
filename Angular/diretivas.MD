**Diretivas**
Diretivas são instruções no DOM.  
*Diretivas estruturais:* Adicionam e removem elementos do DOM.
*Diretivas de atributo:* Modificam os elemntos já existentes. 

---
**ngIf (estrutural)**

É utilizada quando queremos mostrar algum elemento no html condicionalmente. 

    <p *ngIf="propriedade">Sucesso</p>

    ou com else
    <p *ngIf="propriedade; else outraPropriedade">Sucesso</p>

    <ng-template #outraPropriedade>
        <p>Fracaso</p>
    </ng-template>


---
**ngStyle (atributo)**  
Permite a modificação do css associado ao elemento no qual essa diretiva foi inserida.  

    <p [ngStyle]="{backgroundColor: 'red'}">Este parágrafo é vermelho!

    dinamicamente:
    <p [ngStyle]="{backgroundColor: getColor()}">Este parágrafo é vermelho!


---
**ngClass (atributo)**  
Permite a alteração da classe de determinado elemento.

    <p [ngClass]="{bg-green: canShowSuccessMessage === true}"></p>


---
**ngFor (estrutural)**  
Permite que possamos passar dinamicamente um array de dados para o template.  

    <app-carrinho *ngFor="let item of items"></app-carrinho>


    