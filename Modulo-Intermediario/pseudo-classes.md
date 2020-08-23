# Pseudo-Classes

Já vimos algumas pseudo-classes nas seções anteriores como o :hover, e sua sintaxe base seria:

```css
seletor:pseudo-classe {
  propriedade: valor;
}
```

Existem varios tipos de pseudo-classes, cada um com efeito específico para facilitar a vida do desenvolvedor

Lista de pseudo-classes de acordo com a MDN:

```css
:active /* Parecido com hover, link e visited */
:checked /* Quando um elemento de formulario(radio, checkbox e option) estão ativos */
:default /* Elemento padrão */
:dir() /* Relacionado a direção do conteúdo */
:disabled /* Quando está desabilitado */
:empty /* Quando está vazio */
:enabled /* Quando está habilitado */
:first /*  Primeiro elemento */
:first-child /* Primeiro elemento filho */
:first-of-type /*  Primento elemento pelo tipo */
:fullscreen /* Elementos atuais em tela cheia */
:focus /* Aplicado quando o elemento recebe foco */
:hover /* Quando está com o mouse em cima(funciona bem mal no mobile) */
:indeterminate /* Quando está inderteminado(funciona com formulários) */
:in-range /* Relacionado ao atributo min max do <input> */
:invalid /* Quando o elemento é inválido */
:lang() /* Elementos por linguagem */
:last-child /* Ultimo filho */
:last-of-type /* Ultimo por tipo */
:left /* Utilizado a esquerda em conjunto com o @page */
:link /* Quando o elemento é um link */
:not() /* Quando não tem o requisito do parâmetro */
:nth-child() /* Elementos baseado em posição, exemplo: :nth-child(1n) */
:nth-last-child() /* Elemento baseado no ultimo filho */
:nth-last-of-type() /* Elemento baseado no ultimo tipo */
:nth-of-type() /* Elemento por tipo */
:only-child /* Elementos que são necessariamente filhos */
:only-of-type /* Elementos que são especificados no tipo */
:optional /* Elementos que são opcionais */
:out-of-range /* Fora do range do input */
:read-only /*  Relacionado ao input e textarea, quando não está editável*/
:read-write /*  Relacionado ao input e textarea, quando está editável*/
:required /* Elemento requirido */
:right /* Direita relacionado ao @page */
:root /* Elemento base (<html>) */
:scope /*  Elemento que está no escopo */
:target /*  Elemento escolhido*/
:valid /* Elemento válido */
:visited /* Link que já foi visitado */
```

Relaxa, não precisa decorar todos os pseudo-elementos, mas é bom ter a noção dos elementos existentes para facilitar sua vida futuramente.