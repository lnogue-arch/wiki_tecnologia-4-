---
title: Entorno Processing (Estructura, Sistema de Coordenadas y Gráficos 2D)
tags: [processing, programacion_grafica, java, canvas_2d, 4eso]
aliases: [Processing, Gráficos Processing, Sistema de Coordenadas Processing]
---

# Entorno Processing (Estructura, Sistema de Coordenadas y Gráficos 2D)

## ¿Qué es Processing?
**Processing** es un entorno de desarrollo integrado (IDE) y lenguaje de programación visual basado en **Java**, diseñado para la creación de gráficos interactivos, animaciones y experiencias multimedia.

### El Sistema de Coordenadas en Pantalla:
En Processing, el origen de coordenadas **$(0,0)$ está situado en la esquina superior izquierda** del lienzo (*canvas*):
* El eje **$X$** crece hacia la **derecha**.
* El eje **$Y$** crece hacia **abajo**.

```text
  (0,0) -------------> X (width)
    |
    |      (x, y)
    |        •
    v
  Y (height)
```

---

## Estructura Fundamental del Código: `setup()` y `draw()`

```java
void setup() {
  size(600, 400); // Define el ancho y alto de la ventana en píxeles (width=600, height=400)
  background(255); // Pinta el fondo de blanco
}

void draw() {
  // Se ejecuta en bucle a 60 fotogramas por segundo (fps).
  // Aquí se actualizan las animaciones y se redibuja el lienzo.
}
```

---

## Primitivas Gráficas 2D Esenciales:

| Función | Parámetros y Sintaxis | Descripción |
| :--- | :--- | :--- |
| **`point()`** | `point(x, y)` | Dibuja un punto en las coordenadas $(x, y)$. |
| **`line()`** | `line(x1, y1, x2, y2)` | Dibuja un segmento recto desde $(x_1, y_1)$ hasta $(x_2, y_2)$. |
| **`rect()`** | `rect(x, y, ancho, alto)` | Dibuja un rectángulo con esquina superior izquierda en $(x, y)$. |
| **`ellipse()`** | `ellipse(x, y, ancho, alto)` | Dibuja una elipse/círculo centrada en $(x, y)$. |
| **`triangle()`**| `triangle(x1, y1, x2, y2, x3, y3)` | Dibuja un triángulo uniendo los 3 vértices dados. |

---

## Gestión del Color y del Trazo:

* **Colores en Escala de Grises**: Un solo parámetro de $0$ (negro absoluto) a $255$ (blanco puro).
* **Colores RGB**: Tres parámetros `(R, G, B)` de $0$ a $255$ (ej. `fill(255, 0, 0)` para rojo puro).
* **Transparencia (Canal Alfa)**: Cuarto parámetro `(R, G, B, Alfa)` de $0$ (transparente) a $255$ (opaco).
* **`background(r, g, b)`**: Pinta todo el lienzo del color especificado.
* **`fill(r, g, b)`**: Define el color de relleno de las figuras siguientes.
* **`noFill()`**: Desactiva el relleno interior (figura hueca).
* **`stroke(r, g, b)`**: Define el color del borde o trazo.
* **`strokeWeight(grosor)`**: Define el grosor del trazo en píxeles.
* **`noStroke()`**: Elimina el borde exterior.

---

## ¿Por qué importa?
Permite a los estudiantes comprender de forma visual e intuitiva la lógica algorítmica, variables y estructuras de control antes de programar robots físicos.

---

## ¿Cómo se aplica o relaciona?
* Consulta la guía de ejercicios prácticos en [[guia_programacion_processing_de_cero_a_interactivo]].
* Avanza hacia el control con ratón y variables en [[interactividad_y_variables_processing]].
