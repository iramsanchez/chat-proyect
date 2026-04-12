---
name: landing-page-editorial
description: Usa este skill cuando se necesite crear, rehacer o estandarizar una landing page HTML para que siga el formato editorial e institucional de `reformas-electorales.html`, con la misma jerarquia visual, paleta sobria, secciones por bloques, navegacion sticky y tarjetas de contenido desplegable.
---

# Landing Page Editorial

Usa este skill para mantener un formato consistente en todas las landing pages del proyecto.

## Objetivo

Replicar el lenguaje visual y estructural de `reformas-electorales.html` sin copiar el contenido literal.

## Patrón base obligatorio

Cada landing debe conservar esta estructura, en este orden:

1. `header` institucional con acento superior, patron sutil, badge, titulo principal, subtitulo y ficha lateral de autor o entidad.
2. `nav.blocks-nav` sticky con anclas internas hacia los bloques principales.
3. `intro-strip` con 2 a 4 metricas cortas y un texto de contexto.
4. `main` con secciones `.bloque`.
5. Dentro de cada `.bloque`, una cabecera con numero grande, titulo, subtitulo y contador de piezas.
6. Dentro de cada bloque, varias `.timeline-card` o tarjetas equivalentes de contenido.
7. `footer` editorial con descripcion del proyecto y enlaces internos.

## Reglas visuales

- Mantener una estetica institucional, sobria y academica.
- Usar contraste alto y fondo claro calido.
- Conservar jerarquia serif para titulos y sans-serif para cuerpo.
- Evitar layouts genericos de marketing, gradientes llamativos, colores neon o botones agresivos.
- Usar bordes finos, sombras suaves y radios pequenos.
- El color acento principal debe vivir en una familia vino/borgona; el secundario en una familia dorado/arena.

## Tokens de diseño

Lee [references/design-system.md](references/design-system.md) antes de crear una landing nueva o refactorizar una existente. Ahi estan la paleta, tipografia, espaciado, componentes y comportamiento.

## Convenciones HTML/CSS

- Preferir HTML autocontenido con `style` y `script` inline solo cuando el proyecto sea una landing unica.
- Si la landing crece o se reutiliza entre paginas, separar tokens y componentes en CSS compartido.
- Usar nombres de clase semanticos compatibles con el patron actual:
  - `header-inner`
  - `blocks-nav`
  - `intro-strip`
  - `bloque`
  - `bloque-header`
  - `timeline-card`
  - `card-header`
  - `milestones`
  - `coming-soon`
- Mantener `max-width: 1200px` para el contenedor principal.

## Comportamiento interactivo

- La navegacion principal debe marcar la seccion activa al hacer scroll.
- Las tarjetas deben poder expandirse y contraerse.
- Si hay embebidos o iframes, mostrar un estado de carga simple.
- Si aun no existe contenido final, usar un placeholder elegante tipo `coming-soon`.

## Responsividad mínima

- En movil, el hero debe pasar a una sola columna.
- El nav sticky debe permitir scroll horizontal.
- Las metricas del intro deben envolver sin romper alineacion.
- El footer debe colapsar a una columna.
- Los elementos decorativos secundarios pueden simplificarse, pero no desaparecer la jerarquia editorial.

## Tono de contenido

- Tono formal, claro y experto.
- Titulos concisos.
- Subtitulos descriptivos, no promocionales.
- Datos o hitos presentados como etiquetas cortas.
- Evitar lenguaje de venta tipo "descubre", "increible", "transforma".

## Checklist de entrega

- La landing conserva la estructura editorial completa.
- La paleta y tipografia respetan el sistema base.
- Las secciones tienen anclas internas claras.
- Las tarjetas tienen estados cerrados y abiertos legibles.
- La version movil mantiene legibilidad y orden.
- El footer cierra con identidad institucional y navegacion.

## Si necesitas detalles

Consulta [references/design-system.md](references/design-system.md) para los componentes y tokens exactos derivados de `reformas-electorales.html`.
