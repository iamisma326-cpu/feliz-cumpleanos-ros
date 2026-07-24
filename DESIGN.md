# Design

<!-- impeccable:design-schema 1 -->

## Visual World

Libro digital animado con estética minimalista-elegante. Cada página simula un libro físico real con efecto 3D de apertura. La experiencia es íntima, romántica y sorprendente.

## Color Strategy

**Restrained** — Neutros elegantes con un acento romántico sutil.

- **Fondo principal:** `#FAF8F5` (crema cálido, como papel de libro)
- **Texto principal:** `#1A1A1A` (casi negro, legible y elegante)
- **Texto secundario:** `#6B6B6B` (gris medio para metadatos)
- **Acento romántico:** `#D4A0A0` (rosa polvo, usado en detalles sutiles)
- **Borde de página:** `#E8E4DF` (sombra suave de papel)
- **Sombra de libro:** `rgba(0,0,0,0.15)` (profundidad 3D)

## Typography

- **Títulos de página:** Playfair Display (serif elegante, italic para romanticismo)
- **Cuerpo de texto:** Inter (sans limpia y moderna)
- **Tamaño base:** 16px cuerpo, 28-36px títulos
- **Estilo:** Párrafos simples, sin ornamento excesivo

## Component Language

- **Libro:** Contenedor 3D con perspective, páginas que rotan en Y desde el borde izquierdo
- **Páginas:** Frente con imagen + texto, dorso con textura sutil
- **Transiciones:** CSS 3D transforms con ease-in-out, 0.8-1.2s duración
- **Indicador:** Puntos de progreso en la parte inferior

## Motion

- **Apertura de página:** rotateY de 0° a -180° con perspective(1200px)
- **Aparición de contenido:** Fade-in + slide-up suave post-transición
- **Elementos decorativos:** Partículas sutiles o pétalos en tránsito
- **Easing:** cubic-bezier(0.645, 0.045, 0.355, 1.000) — suave y orgánico

## Responsive

- Mobile-first: libro ocupa 90vw en móvil, max 500px en desktop
- Touch: swipe izquierda/derecha para cambiar páginas
- Click: clic en bordes para girar página

## Constraints

- Imágenes de Kaoru Hana wa Rin to Saku de internet (placeholder hasta confirmar)
- Sin dependencias externas (HTML/CSS/JS puro)
- Funciona en Chrome, Safari, Firefox (móvil y desktop)
- Sin audio (experiencia visual silenciosa)
