# Tricky — Tres en Línea

**Tres en línea jugable en consola contra la máquina, con tablero visual en ASCII, gestión de turnos, validación de jugadas y detección automática de victoria o empate.**

---

## Cómo funciona

La máquina abre con la casilla central (5) y el jugador responde eligiendo una posición del 1 al 9. El tablero se redibuja después de cada turno:

```
+-------+-------+-------+
|       |       |       |
|   1   |   2   |   3   |
|       |       |       |
+-------+-------+-------+
|       |       |       |
|   4   |   X   |   6   |
|       |       |       |
+-------+-------+-------+
|       |       |       |
|   7   |   8   |   9   |
|       |       |       |
+-------+-------+-------+
```

- **X** = jugada de la máquina
- **O** = jugada del usuario
- Los números restantes indican casillas disponibles

---

## Mecánica del juego

| Componente | Implementación |
|-----------|----------------|
| Tablero | Matriz 3×3, renderizada con bordes ASCII en cada turno |
| Turnos | Recursivos: cada llamada a `Tricky()` representa un ciclo máquina → usuario |
| Jugada de la máquina | Selección aleatoria entre las casillas disponibles (`random.shuffle`) |
| Detección de victoria | 8 conjuntos predefinidos (3 filas, 3 columnas, 2 diagonales) verificados con `issubset()` |
| Empate | Se detecta cuando no quedan casillas disponibles y nadie ha ganado |

### Funciones

| Función | Descripción |
|---------|-------------|
| `azar(lista)` | Baraja las casillas disponibles y devuelve una al azar. |
| `actualizar(P, lista)` | Elimina la casilla elegida por el usuario de las disponibles. |
| `tablero(x)` | Renderiza el tablero con `X`, `O` y números según el estado actual. |
| `Tricky(x, PJ, JIA, JU)` | Función principal recursiva: ejecuta el turno, verifica condiciones de fin y solicita la siguiente jugada. |

---

## Ejemplo de partida

```
Máquina juega: 5 (centro)
Usuario juega: 1 (esquina superior izquierda)
Máquina juega: 7 (aleatorio)
Usuario juega: 9 (esquina inferior derecha)
...
→ Has ganado / La máquina gana / Empate
```

---

## Evolución prevista

La versión actual utiliza jugadas aleatorias como oponente. Futuras iteraciones incorporarán estrategia computada:

- **Análisis de amenazas** — Detectar cuándo el usuario está a una jugada de ganar y bloquear.
- **Evaluación de posiciones** — Priorizar casillas que maximicen las líneas propias abiertas.
- **Minimax** — Algoritmo de búsqueda exhaustiva para encontrar la jugada óptima en cada turno.

---

## Estructura

```
Tricky/
├── README.md
└── Tricky.ipynb   # Juego completo con demo
```

---

## Requisitos

```
python 3.x
```

No requiere dependencias externas (usa `random` de la biblioteca estándar).
