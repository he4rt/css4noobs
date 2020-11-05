# Pseudo-Classes

Pseudo-classes são referências utilizadas através de sufixos nos seletores, para definir um estado especial de um elemento. Este recurso é muito importante para aplicar estilo para situações específicas de maneira performática, evitando seletores extensos em cascata ou aplicação lógica através do Javascript para manipulação dinâmica.

Já vimos algumas pseudo-classes nas seções anteriores como o :hover, sua sintaxe base seria:

```css
seletor:pseudo-classe {
  propriedade: valor;
}
```

Existem múltiplas pseudo-classes, cada uma com aplicação específica para alterar o estilo da página em situações e eventos de fluxo diferentes.

Lista de pseudo-classes de acordo com a MDN complementada por uma pequena descrição utilizada como referência:

| Valor | Descrição |
| --- | --- |
| ```:active``` | Utilizada em links e botões, define se um elemento alvo está ativo pela navegação do usuário |
| ```:checked``` | Quando um elemento de formulário (```radio```, ```checkbox``` e ```option```) estão ativos |
| ```:default``` | Elemento(s) padrão(ões) de um formulário |
| ```:dir()``` | Relacionado a direção do conteúdo |
| ```:disabled``` | Quando está desabilitado |
| ```:empty``` | Quando está vazio |
| ```:enabled``` | Quando está habilitado |
| ```:first``` | Primeiro elemento |
| ```:first-child``` | Primeiro elemento filho |
| ```:first-of-type``` | Primeiro elemento pelo tipo |
| ```:fullscreen``` | Elementos atuais em tela cheia |
| ```:focus``` | Aplicado quando o elemento recebe foco |
| ```:hover``` | Quando está com o mouse em cima |
| ```:indeterminate``` | Quando está indeterminado (funciona com formulários) |
| ```:in-range``` | Aplicado aos elementos ```<input>``` os quais o **valor atual** está compreendido no intervalo dos atributos **min** e **max** do mesmo |
| ```:invalid``` | Aplicado à **elementos inválidos** de um *formulário* |
| ```:lang()``` | Elementos por língua |
| ```:last-child``` | Último filho |
| ```:last-of-type``` | Último por tipo/grupo de elementos |
| ```:left``` | Utilizado a esquerda em conjunto com o ```@page``` |
| ```:link``` | Quando o elemento é um link |
| ```:not()``` | Quando não tem o requisito do parâmetro |
| ```:nth-child()``` | Elementos baseado em posição, exemplo: ```:nth-child(1n)``` |
| ```:nth-last-child()``` | Elemento baseado no último filho |
| ```:nth-last-of-type()``` | Elemento baseado no último tipo/grupo de elementos |
| ```:nth-of-type()``` | Elemento por tipo/grupo de elementos |
| ```:only-child``` | Elementos que são necessariamente filhos |
| ```:only-of-type``` | Elementos que são especificados no tipo/grupo de elementos |
| ```:optional``` | Elementos de um formulário que são opcionais |
| ```:out-of-range``` | Aplicado aos elementos ```<input>``` os quais o **valor atual não está compreendido** no intervalo dos atributos **min** e **max** do mesmo |
| ```:read-only``` | Relacionado ao ```input``` e ```textarea```, quando não está editável |
| ```:read-write``` | Relacionado ao ```input``` e ```textarea```, quando está editável |
| ```:required``` | Elemento de um formulário requirido |
| ```:right``` | Direita relacionado ao ```@page``` |
| ```:root``` | Elemento base ```<html>``` |
| ```:scope``` | Elemento que está no escopo |
| ```:target``` | Elemento selecionado através de um identificador único compreendido na URL |
| ```:valid``` | Elemento de um formulário válido |
| ```:visited``` | Link que já foi visitado |

Relaxa, não precisa decorar todos os pseudo-elementos, mas é bom ter a noção dos elementos existentes para facilitar sua vida futuramente.