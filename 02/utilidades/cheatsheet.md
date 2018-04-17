# Seletores de CSS

> Tradução de https://gist.github.com/smutnyleszek/809a69dd05e1d5f12d01

## Seletores de Elementos

**Elementos** -- seleciona todos os elementos `h2` na página

``` CSS
h2 {
    foo: bar;
}
```

**Groupos** -- seleciona todos os elementos `h1`, `h2` e `h3` na página

``` CSS
h1, h2, h3 {
    foo: bar;
}
```


## Classes e IDs

**Classes** -- seleciona todos os elementos com o atributo classe contendo `foo` ou somente elementos `p` com esta classe

``` CSS
.foo {
    bar: fum;
}
p.foo {
    bar: fum;
}
```

**ID** -- seleciona elementos com o id `baz`

``` CSS
#foo {
    bar: fum;
}
```


## Seletores contextuais

**Descendentes** -- seleciona todos os elementos  `p` filhos de `#foo`, ou filhos de filhos de `#foo` e assim por diante infinitamente

``` CSS
#foo p {
    bar: fum;
}
```

**Irmãos** -- seleciona o elemento irmão `p` que vier imediatamente depois de um elemento `h2`

``` CSS
h2 + p {
    foo: bar;
}
```

**Filhos** -- seleciona todos os elementos `p` que forem filhos diretos de `#foo`

``` CSS
#foo > p {
    bar: fum;
}
```

**Irmãos no geral** -- seleciona todos os elementos `p` que sejam irmãos de elementos `h2`

``` CSS
h2 ~ p {
    foo: bar;
}
```


## Pseudo seletores 


### Pseudo seletores para links e inputs

**Link não visitado** -- se aplica a elementos `a` que não foram visitados pelo usuário ainda

``` CSS
a:link {
    foo: bar;
}
```

**Links visitados** -- se aplica a elamentos `a` que já foram visitados pelo usuário

``` CSS
a:visited {
    foo: bar;
}
```

**Elementos focados** -- se aplica a todos os elementos com a classe `.foo` the estão prontos para interação

``` CSS
.foo:focus {
    bar: fum;
}
```

**Elementos com hover** -- se aplica quando o mouse está sobre o elemento `.foo`

``` CSS
.foo:hover {
    bar: fum;
}
```

**Elementos ativos** -- se aplica quando elementos com a classe `.foo` estão no meio de um click

``` CSS
.foo:active {
    bar: fum;
}
```


### Pseudo seletores que se referem a irmãos

**Primeiro filho** -- seleciona elementos com a classe `.foo` quando eles são o primeiro filho de seus pais

``` CSS
.foo:first-child {
    bar: fum;
}
```

**Último filho** -- seleciona elementos com a classe  `.foo` quando eles são os últimos filhos de seus pais

``` CSS
.foo:last-child {
    bar: fum;
}
```

**Único filho** -- seleciona elementos com a classe `.foo` quando eles são os únicos filhos de seus pais

``` CSS
.foo:only-child {
    bar: fum;
}
```

**Primeiro do tipo** -- seleciona elementos `h2` quando eles são o primeiro de seu tipo dentro de seus pais

``` CSS
h2:first-of-type {
    foo: bar;
}
```

**Último do tipo** -- seleciona elementos `h2` quando eles são o último de seu tipo dentro de seus pais

``` CSS
h2:last-of-type {
    foo: bar;
}
```

**Único do tipo** -- seleciona elementos `h2` quando eles são o único de seu tipo dentro de seus pais

``` CSS
h2:only-of-type {
    foo: bar;
}
```

**Nth child** -- seleciona o `n`ésimo elemento `.foo` dentro de seus pais

``` CSS
.foo:nth-child(n) {
    bar: fum;
}
```

**Nth last child** -- seleciona o `n`ésimo elemento `.foo` dentro de seus pais, contando de trás pra frente

``` CSS
.foo:nth-last-child(n) {
    bar: fum;
}
```

**Nth of type** -- seleciona o `n`ésimo elemento do tipo `h2` dentro de seus pais

``` CSS
h2:nth-of-type(n) {
    foo: bar;
}
```

**Nth last of type** -- seleciona o `n`ésimo elemento do tipo `h2` dentro de seus pais, contando de trás pra frente

``` CSS
h2:nth-last-of-type(n) {
    foo: bar;
}
```

Valores úteis para `n`:

- `odd` ou `2n+1` -- todo filho ímpar
- `even` ou `2n` -- todo filho par
- `n` -- todo `n`ésimo filho
- `3n` -- todo filho múltiplo de três (3, 6, 9, ...)
- `3n+1` -- (todo filho múltiplo de três) + 1 (1, 4, 7, ...)
- `n+6` -- todos menos os primeiro cinco filhos (6, 7, 8, ...)
- `-n+5` -- somente os primeiro cinco filhos (1, 2, ..., 5)


### Seletores de pseudo elementos

**Primeira letra** -- seleciona a primeira letra do elemento `.foo` , comumente usado em conjunto com  `:first-child` para selecionar o primeiro parágrafo de um texto

``` CSS
.foo::first-letter {
    bar: fum;
}
```

**Primeira linha** -- seleciona a primeira linha do elemento `.foo` ,  comumente usado em conjunto com  `:first-child` para selecionar o primeiro parágrafo de um texto

``` CSS
.foo::first-line {
    bar: fum;
}
```

**Antes** -- adiciona conteúdo customizado antes do elemento `.foo` quando usado com a propriedade `content`

``` CSS
.foo::before {
    bar: fum;
    content: 'baz';
}
```

**Depois** -- adiciona conteúdo customizado antes do elemento `.foo` quando usado com a propriedade `content`

``` CSS
.foo::after {
    bar: fum;
    content: 'baz';
}
```


## Seletores de atributos

**Presente** -- seleciona elementos foo `.foo` com o atributo `bar` presente, independente de seu valor

``` CSS
.foo[bar] {
    fum: baz;
}
```

**Exato** -- seleciona elementos `.foo` onde o atributo `bar` tem o valor exato `fum`

``` CSS
.foo[bar="fum"] {
    baz: qux;
}
```

**Separados por espaços vazios** -- seleciona elementos `.foo` onde o atributo `bar` contém o valor parcial `fum` separado por espaços em branco 

``` CSS
.foo[bar~="fum"] {
    baz: qux;
}
```

**Separados por hífens** -- seleciona elementos `.foo` onde o atributo `bar` contêm o valor parcial `fum` imediatamente seguido de um hífen (`-`) 

``` CSS
.foo[bar|="fum"] {
    baz: qux;
}
```

**Começa com** -- seleciona elementos `.foo` onde o atributo `bar` começa com `fum`

``` CSS
.foo[bar^="fum"] {
    baz: qux;
}
```

**Termina com** -- seleciona elementos `.foo` onde o atributo `bar` termina com `fum`

``` CSS
.foo[bar$="fum"] {
    baz: qux;
}
```

**Contém** -- seleciona elementos `.foo` onde o atributo `bar` contém a string `fum` seguida e precidida por qualquer caractere

``` CSS
.foo[bar*="fum"] {
    baz: qux;
}
```


## Misc

**Not** -- seleciona elementos `.foo` que NÃO são elementos `.bar`

``` CSS
.foo:not(.bar) {
    fum: baz;
}
```

**Root** -- seleciona o pai de nível mais alto no DOM

``` CSS
:root {
    foo: bar;
}
```

**Empty** -- seleciona elementos `.foo` que não tem filhos nem espaços em branco dentro

``` CSS
.foo:empty {
    bar: fum;
}
```
