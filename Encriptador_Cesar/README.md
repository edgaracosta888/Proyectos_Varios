# Encriptador César Mejorado

**Implementación del cifrado César extendido a todo el espectro de caracteres ASCII imprimibles — letras, dígitos, puntuación y espacios — en lugar del alfabeto clásico de 26 letras.**

---

## La mejora

El cifrado César clásico desplaza cada letra del alfabeto una cantidad fija de posiciones. Su limitación: solo opera sobre 26 caracteres (las letras), dejando dígitos, signos y espacios sin encriptar, lo que facilita enormemente el criptoanálisis.

Esta versión extiende el alfabeto de cifrado a **99 caracteres**:

```
a-z  A-Z  0-9  !"#$%&'()*+,-./:;<=>?@[\]^_`{|}~  espacios y whitespace
 26 + 26 + 10 +              32                   +    5     = 99
```

Al incluir todo el espectro, un espacio ya no se ve como espacio en el texto cifrado, un dígito puede convertirse en un signo de puntuación, y viceversa. El espacio de búsqueda para fuerza bruta pasa de 26 a 99 posibles desplazamientos.

---

## Funciones

| Función | Descripción |
|---------|-------------|
| `Encriptado_Cesar_Mejorado()` | Solicita texto y clave numérica, desplaza cada carácter `n` posiciones en el alfabeto extendido (con wrap-around) y retorna el texto cifrado. |
| `Desencriptado_Cesar_Mejorado()` | Operación inversa: solicita texto cifrado y clave, desplaza `-n` posiciones para recuperar el texto original. |

### Funciones auxiliares

| Función | Rol |
|---------|-----|
| `spliter()` | Captura texto y clave del usuario. |
| `encriptacion()` | Aplica el desplazamiento positivo carácter por carácter. |
| `desencriptar()` | Captura texto cifrado y clave. |
| `desencriptacion()` | Aplica el desplazamiento negativo carácter por carácter. |
| `lista_a_texto(lista)` | Convierte la lista de caracteres de vuelta a string. |

---

## Ejemplo

```
Texto original:    Hola Mundo 2026!
Clave:             7
Texto cifrado:     Ovshy|}ukv'9569(
```

```
Texto cifrado:     Ovshy|}ukv'9569(
Clave:             7
Texto recuperado:  Hola Mundo 2026!
```

---

## Estructura

```
Encriptador_Cesar/
├── README.md
└── Encriptador_Cesar.ipynb   # Encriptación + desencriptación con demo
```

---

## Requisitos

```
python 3.x
```

No requiere dependencias externas (usa `string` de la biblioteca estándar).
