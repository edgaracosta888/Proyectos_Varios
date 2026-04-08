# Display LED

**Renderiza cualquier número entero como un display LED de 7 segmentos en consola, usando solo caracteres `#` y espacios — tres versiones que evolucionan desde un enfoque directo hasta un diseño funcional limpio.**

---

## La idea

Tomar un número entero y dibujarlo en la terminal como si fuese un display LED digital, donde cada dígito ocupa una grilla de 3×5 caracteres:

```
###    #  ###  ###  # #  ###  ###  ###  ###  ###
# #    #    #    #  # #  #    #      #  # #  # #
# #    #  ###  ###  ###  ###  ###    #  ###  ###
# #    #  #      #    #    #  # #    #  # #    #
###    #  ###  ###    #  ###  ###    #  ###  ###
```

---

## Versiones

El notebook presenta tres iteraciones del mismo problema, cada una con un enfoque diferente:

| Versión | Enfoque | Características |
|---------|---------|-----------------|
| `led_v1()` | Diccionario directo | Cada dígito se define manualmente como lista de 5 strings. Alineación por longitud de string. |
| `led_v2()` | Diccionario con bloques reutilizables | Introduce `matriz = ['###', '#']` como bloques base y construye los dígitos combinándolos. Reduce redundancia. |
| `led_v3()` | Diseño funcional | Separa responsabilidades: `ingresar_numero()` valida, `print_led()` renderiza con un generador compacto. Diccionario `DIGITS` como constante global con tuplas normalizadas a 3 caracteres. |

### Evolución del diseño

```
v1: Todo en una función — definición, input, alineación manual, impresión
 ↓
v2: Misma estructura, pero reduce repetición con bloques base (matriz)
 ↓
v3: Separación de responsabilidades — constante global, función pura de renderizado, generador
```

---

## Ejemplo

```python
led_v3()
# Introduce un número entero: 2025
#
# ###  ###  ###  ###
#   #  # #    #  #
# ###  # #  ###  ###
# #    # #  #      #
# ###  ###  ###  ###
```

---

## Estructura

```
Display_LED/
├── README.md
└── Display_LED.ipynb   # Tres versiones del display LED
```

---

## Requisitos

```
python 3.x
```

No requiere dependencias externas.
