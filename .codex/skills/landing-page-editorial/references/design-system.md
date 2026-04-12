# Sistema visual derivado de `reformas-electorales.html`

## Resumen

La landing de referencia usa un estilo editorial institucional:

- hero solemne con color borgona
- tipografia serif para jerarquia
- sans-serif para lectura continua
- navegacion sticky por bloques
- tarjetas modulares con expansion
- fondos claros y calidos
- detalles dorados discretos

## Paleta base

```css
:root {
  --ine-burgundy: #6B1A2A;
  --ine-gold: #C8A84B;
  --ine-gold-light: #E8D08A;
  --ine-dark: #1A1A2E;
  --ine-gray-dark: #2D2D3A;
  --ine-gray-mid: #5A5A6E;
  --ine-gray-light: #F0EDE8;
  --ine-cream: #FAF8F4;
  --ine-white: #FFFFFF;
  --ine-red-soft: #8B2340;
  --ine-gold-dark: #9A7A28;
}
```

## Tipografia

- Titulos y numeros destacados: `Playfair Display`, serif
- Cuerpo y navegacion: `Source Sans 3`, sans-serif

## Layout

- ancho maximo de contenido: `1200px`
- padding horizontal habitual: `2rem`
- espaciado entre bloques: `4rem`
- padding principal de `main`: `3rem 2rem 5rem`

## Componentes obligatorios

## 1. Header

Debe incluir:

- franja superior dorada o acento lineal
- patron de fondo muy sutil
- badge pequeno en mayusculas
- `h1` principal con una palabra o frase destacable en color acento
- subtitulo descriptivo
- tarjeta lateral de autor, firma, area o institucion

## 2. Navegacion sticky

Debe incluir:

- fondo oscuro
- enlaces internos a secciones
- indicador numerico pequeño
- estado activo con dorado
- scroll horizontal en pantallas pequeñas

## 3. Intro strip

Debe incluir:

- mini metricas con numero grande y label pequeno
- divisores verticales
- un texto contextual con borde izquierdo en dorado

## 4. Bloques de contenido

Cada bloque debe incluir:

- numero grande en transparencia
- titulo con serif
- subtitulo explicativo
- contador de piezas en badge pequeño

## 5. Tarjetas de contenido

Patron recomendado:

- fondo blanco
- borde fino
- sombra ligera
- barra lateral de color acento
- etiqueta de tipo
- titulo
- descripcion breve
- lista de hitos o tags
- icono de toggle circular
- cuerpo ocultable para embebido, detalle o placeholder

## Tipos de tarjeta

Si hace sentido para el contenido, reutiliza estas variantes:

- `type-original`
- `type-nuevo`
- `type-reenfocado`

Si no aplican, crear variantes equivalentes pero mantener el mismo peso visual.

## Estados vacios

Cuando falte contenido final:

- usar bloque `coming-soon`
- icono simple en circulo
- titulo corto
- parrafo breve en tono editorial

## Interaccion

Javascript minimo esperado:

- `toggleCard(id)` para abrir y cerrar tarjetas
- helper de carga para iframes o embebidos
- `IntersectionObserver` para sincronizar nav sticky con la seccion visible

## Responsive

Breakpoint base observado: `768px`

En movil:

- hero en una sola columna
- tarjeta lateral a ancho completo
- footer en una columna
- contador de bloque opcionalmente oculto
- nav con scroll horizontal

## Tono y estilo editorial

- academico
- institucional
- preciso
- sin lenguaje comercial
- sin CTA invasivos
- sin visuales exagerados

## Plantilla estructural sugerida

```html
<header>...</header>
<nav class="blocks-nav">...</nav>
<div class="intro-strip">...</div>
<main>
  <section class="bloque" id="bloque1">...</section>
  <section class="bloque" id="bloque2">...</section>
</main>
<footer>...</footer>
<script>
  // toggleCard + observer
</script>
```

## Decisiones que deben mantenerse en futuras landings

- misma jerarquia de lectura de arriba hacia abajo
- misma familia de colores, aunque cambie ligeramente el tema
- misma logica de navegacion interna
- mismo lenguaje de tarjetas modulares
- mismo tono institucional en textos

## Decisiones que si pueden variar

- numero de bloques
- numero de metricas del intro
- tipo de contenido dentro de cada tarjeta
- presencia de iframes, embeds, imagenes o placeholders
- nombre del autor o institucion
