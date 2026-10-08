# Bloques

Juego tipo Tetris que corre en el navegador. Es un solo archivo (`index.html`), sin instalar nada ni usar librerías.

## Cómo jugar

| Tecla | Acción |
|---|---|
| ← → | Mover la pieza |
| ↑ o X | Rotar |
| ↓ | Bajar más rápido |
| Espacio | Caída directa |
| C o Shift | Reservar pieza |
| P o Esc | Pausa |

En celulares y tabletas aparecen botones en pantalla.

- Cada 10 líneas subes de nivel y las piezas caen más rápido.
- Puntos por líneas: 1 = 100, 2 = 300, 3 = 500, 4 = 800 (multiplicado por el nivel).
- Tu mejor puntaje se guarda en el navegador (`localStorage`).
- El juego se pausa solo si cambias de pestaña.

## Probarlo en tu computadora

Abre `index.html` con doble clic.

## Publicarlo con GitHub Pages

1. Crea un repositorio nuevo en GitHub y sube `index.html` y este `README.md`.
2. Entra a **Settings → Pages**.
3. En **Build and deployment**, elige **Deploy from a branch**, rama `main`, carpeta `/ (root)`.
4. Guarda. En un minuto el juego queda en `https://TU-USUARIO.github.io/NOMBRE-DEL-REPO/`.

## Personalizar

- Colores de las piezas: objeto `COLORS` en el script.
- Velocidad: la línea `Math.max(70, 800 * Math.pow(.85, level-1))` (milisegundos por caída).
- Tamaño del tablero: constantes `COLS` y `ROWS` (si los cambias, ajusta también el `width`/`height` del canvas `#board`).
