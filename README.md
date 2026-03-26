# Proyectos_Varios

Repositorio personal para agrupar proyectos diversos de programación y lógica aplicada.
Aquí se irán incorporando notebooks y códigos de distintos temas, desde visualizaciones simples hasta juegos y ejercicios de lógica.

## Proyectos

### 1. Display_LED
- **Carpeta:** `Display_LED/`
- **Descripción breve:**
	Proyecto en Python para mostrar números enteros en formato LED usando caracteres ASCII.
	Incluye varias versiones de implementación, donde la versión funcional está optimizada en legibilidad y eficiencia.

### 2. Tricky (Tres en Línea)
- **Carpeta:** `Tricky/`
- **Descripción breve:**
	Implementación del juego Tres en línea en Python para practicar estructuras de control y lógica de juego.
	Incluye gestión de turnos, validación de jugadas y verificación de victoria/empate.
	En la versión actual, la computadora juega como oponente con movimientos aleatorios (sin estrategia).

### 3. Encriptador y Desencriptador Cesar mejorado
- **Carpeta:** `Encriptador_Cesar/`
Este proyecto implementa una versión ampliada del clásico cifrado César, diseñada para trabajar no solo con letras, sino también con una gran variedad de caracteres de uso real en textos modernos.

El cifrado César tradicional es un método de sustitución en el que cada letra de un mensaje se desplaza un número fijo de posiciones dentro del alfabeto. Por ejemplo, con una clave de desplazamiento de 3, la letra A pasa a ser D, B pasa a E, etc. Es una técnica histórica, simple y muy útil para comprender los fundamentos de la criptografía.

En esta versión, el enfoque está mejorado porque no se limita al alfabeto básico. En lugar de cifrar únicamente letras, el sistema trabaja con un conjunto mucho más completo que incluye:

- Letras mayúsculas y minúsculas (A-Z, a-z)
- Dígitos (0-9)
- Signos de puntuación
- Espacios y caracteres en blanco

Gracias a esto, el encriptador puede procesar textos más realistas (frases completas, números, símbolos, etc.) sin perder información ni requerir limpieza previa del mensaje.

#### ¿Cómo funciona el encriptador?
1. El usuario introduce un texto.
2. El programa solicita una clave numérica (desplazamiento).
3. Cada carácter del texto se busca en un alfabeto extendido.
4. Se desplaza su posición según la clave.
5. Si el desplazamiento supera la longitud total del alfabeto, se aplica ajuste circular (módulo), para continuar desde el inicio.
6. Finalmente, se reconstruye y devuelve el texto cifrado.

#### ¿Por qué esta versión es “mejorada”?
- Mayor compatibilidad de caracteres: no falla con números, símbolos o espacios.
- Más práctica para casos reales: permite cifrar mensajes más naturales, no solo palabras alfabéticas.

#### Desencriptador César Mejorado
El proyecto también incluye el proceso inverso: el desencriptador.

Su lógica consiste en:

1. Recibir el texto cifrado y la clave.
2. Ubicar cada carácter dentro del mismo alfabeto extendido.
3. Restar el desplazamiento en lugar de sumarlo.
4. Aplicar ajuste circular cuando la posición se sale del rango.
5. Reconstruir el texto original.
6. Esto garantiza que, usando la misma clave con la que se cifró el mensaje, se pueda recuperar el contenido original de forma precisa.


## Estructura

```text
Proyectos_Varios/
├── README.md
├── Display_LED/
├── Tricky/
├── Encriptador_Cesar/
```

> La estructura irá creciendo a medida que se agreguen nuevos proyectos.

## Notas

- Cada subcarpeta representa un proyecto independiente.
- Se prioriza código claro, incremental y fácil de mantener.
- Este repositorio se encuentra en actualización continua.