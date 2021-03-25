# curso-completo-de-sass-scss-do-iniciante-ao-avancado
 Curso Completo de SASS/SCSS: do Iniciante ao Avançado


## Instalar

```
npm install -g sass
```

## Compilar

```
sass source/stylesheets/index.scss build/stylesheets/index.css
```

### Exeemplos
```
sass arquivo.sass arquivo.scss
sass arquivo.scss arquico.css
```

## Modo Watch

### Monitorar Arquivo

```
sass --watch arquivo.scss:arquivo.css 
```

### Monitorar Pastas

```
sass --watch scss:css 
```

## Interface Web

Link: [SASS Meister](https://www.sassmeister.com/)

## Formatos de Saída

- nested
- expanded
- compact
- compressed

```
sass style.scss style.css --style compact
sass --watch scss:css --style compressed
```

## Comentários

### Comentário Normal
```
/* comentario */
```

### Comentário somente para o SASS
```
// comentario
```

### Comentário para Saída Compressed

```
/*! comentario */
```

## Interpolação

- Entrada

```
$cor: black;
$propriedade: font;

.#{$cor} {
  color: $cor;
  #{propriedade}-size: 14px;
}
```

- Saída

```
.black {
  color: black;
  font-size: 14px;
}
```

## Namespace

- Entrada

```
$cor: black;
$propriedade: font;

.#{$cor} {
  color: $cor;
  #{propriedade}: {
    size: 14px;
    style: italic;
  }
}
```

- Saída

```
.black {
  color: black;
  font-size: 14px;
  font-style: italic;
}
```

## Variável

- global
- default

```
$color: red;
$color2: red !global;
$color3: blue !default; // define a variável se ela não foi definida ainda
```

## Tipos de Dados
- Números (por exemplo 1.5, 10, 250px)
- Cadeias de texto, com e sem aspas (por exemplo "lateral", 'content', principal)
- Cores (por exemplo red, #cccccc, rgba(255, 255, 0, 0.8))
- Booleanos (por exemplo true, false)
- Nulos (por exemplo: null)
- Listas de valores, separados por espaços ou vírgulas (por exemplo 1.5em 2em 0 6em ou Helvetica, Arial, sans-serif)
- Mapas de um valor para outro (por exemplo (key1: value1, key2: value2))


## Acessar o Shell do SASS Script

```
sass -i
```

## Import

```
@import 'reset.sass';
@import 'reset';
@import 'variaveis.scss';
@import "arquivo.scss" screen;
@import url('https://fonts.googleapis.com/css?family=Roboto');
```