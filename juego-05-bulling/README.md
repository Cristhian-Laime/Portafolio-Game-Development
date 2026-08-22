# Mica — un video, muchos caminos

Historia interactiva con minijuegos sobre lo que pasa cuando un video privado se viraliza sin permiso. El jugador toma las decisiones de Mica y ve cómo cada camino la lleva a un final distinto.

---

## Descripción

Mica sube un video bailando frente al espejo. Al día siguiente, un fragmento recortado ya circula fuera de su control. A partir de ahí, el jugador decide cómo reacciona: desaparecer, defenderse o buscar ayuda. Cada decisión abre una rama narrativa distinta, con su propio minijuego, su propio ritmo visual y su propio final.

El objetivo no es "ganar", sino recorrer las consecuencias de cada camino: aislamiento, conflicto o recuperación.

---

## Cómo se juega

- La historia avanza combinando **pantallas de texto**, **decisiones** y **minijuegos cortos** jugados con teclado o controles táctiles en pantalla.
- Después de cada decisión importante, un **diagrama de árbol** muestra visualmente qué camino se tomó y qué otros existían.
- Al final de cada ruta se despliega una **pantalla de cierre** con el árbol completo de decisiones y la posibilidad de volver a jugar.

### Controles

| Minijuego | Mecánica | Controles |
|---|---|---|
| Ensayo / baile | Cambiar de carril para recoger chispas | ← → / botones laterales |
| Avalancha de notificaciones | Esquivar objetos que caen | ← → / botones laterales |
| Encierro | Moverse en un cuarto que se encoge | Flechas direccionales / D-pad |
| Ola de mensajes | Esquivar burbujas en movimiento vertical | ↑ ↓ / botones verticales |
| Acercarse | Caminar hacia un personaje de confianza | Flechas direccionales / D-pad |

En dispositivos táctiles, los controles aparecen automáticamente debajo de la pantalla de juego.

---

## Ramas y finales

| Decisión inicial | Camino | Final |
|---|---|---|
| Borrar todo y desaparecer | Aislamiento progresivo, el espacio personal se cierra | **Aislamiento** |
| Responder y defenderse | El conflicto se extiende y no termina | **Conflicto** |
| Contarle a alguien de confianza | Elegir a un amigo, familiar o profesor y acercarse a esa persona | **Recuperación** |

La rama de ayuda se ramifica una vez más según a quién elige contarle Mica (una amiga, un hermano o una profesora), aunque todas convergen en el mismo final de recuperación.

---

## Aspectos técnicos

- **Tecnología:** HTML5, CSS y JavaScript puro, sin frameworks ni librerías externas. Un solo archivo autocontenido.
- **Narrativa:** manejada por funciones de transición entre pantallas (`showText`, `showChoices`) con fundidos animados.
- **Diagramas de decisión:** generados dinámicamente como SVG a partir del estado de la partida (`state.decision1`, `state.subDecision`).
- **Minijuegos:** implementados sobre `<canvas>` con un bucle de animación por `requestAnimationFrame`, con lógica independiente para cada mecánica (esquivar, recolectar, desplazarse).
- **Responsive:** se adapta a pantallas móviles; los controles cambian de teclado a botones táctiles según el dispositivo.
- **Accesibilidad:** respeta `prefers-reduced-motion` desactivando animaciones cuando el sistema lo solicita.

---

## Estructura sugerida del proyecto

```
mica/
├── mica.html          # Juego completo (HTML + CSS + JS en un solo archivo)
├── screenshots/        # Capturas de las distintas pantallas y finales
└── README.md
```

---

## Apoyo de IA

<!-- Describe aquí qué partes fueron desarrolladas con apoyo de IA (código, arte, texto, testing, etc.) -->
[Describe qué elementos del desarrollo usaron asistencia de IA]

## Qué aprendí

<!-- TODO -->
[Reflexiona brevemente: manejo de canvas, diseño de ramas narrativas, animaciones SVG, diseño de UI, etc.]

## Qué mejoraría en una siguiente versión

<!-- TODO -->
[Sonido, guardado de progreso, más finales, ajuste de dificultad de los minijuegos, etc.]

---

## Nota sobre el contenido

Este proyecto aborda temas sensibles como el acoso en línea y la exposición no consentida de contenido personal. Está pensado como una experiencia educativa y reflexiva, no como una guía de comportamiento; ninguno de los finales busca decir cuál es "la decisión correcta", sino mostrar consecuencias posibles.

---

Proyecto desarrollado para la asignatura **Game Development** — Introducción al desarrollo de videojuegos.
