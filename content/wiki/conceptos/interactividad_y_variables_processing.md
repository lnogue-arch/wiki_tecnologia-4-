---
title: Interactividad y Variables del Sistema en Processing
tags: [processing, interactividad, variables, eventos, condicionales, 4eso]
aliases: [Variables Processing, mouseX mouseY, Condicionales Processing]
---

# Interactividad y Variables del Sistema en Processing

## 1. Variables del Sistema Integradas

Processing proporciona variables especiales accesibles en cualquier parte del programa:

* **`width`**: Ancho total de la ventana en píxeles (definido en `size()`).
* **`height`**: Alto total de la ventana en píxeles.
* **`mouseX`**: Coordenada $X$ actual del cursor del ratón.
* **`mouseY`**: Coordenada $Y$ actual del cursor del ratón.
* **`pmouseX` / `pmouseY`**: Coordenadas $X, Y$ del ratón en el fotograma (*frame*) anterior.
* **`frameCount`**: Número de fotogramas transcurridos desde el inicio del programa.

---

## 2. Pizarra de Dibujo Interactiva (Ejemplo con Ratón):

```java
void setup() {
  size(800, 600);
  background(255);
}

void draw() {
  if (mousePressed) {
    stroke(0);
    strokeWeight(4);
    line(pmouseX, pmouseY, mouseX, mouseY); // Traza continua suave
  }
}
```

---

## 3. Estructuras de Control y Lógica

### A. Condicionales `if - else if - else`:
Permiten ejecutar código según la posición del cursor o el estado de teclas:

```java
void draw() {
  background(200);
  
  if (mouseX < width / 2) {
    // Si el ratón está en la mitad izquierda
    fill(255, 0, 0); // Rojo
  } else {
    // Si el ratón está en la mitad derecha
    fill(0, 0, 255); // Azul
  }
  
  ellipse(mouseX, mouseY, 50, 50);
}
```

### B. Bucles `for` (Repetición y Patrones Geométricos):
Permiten dibujar cuadrículas, dianas o secuencias de figuras con una sola instrucción:

```java
// Dibuja una serie de 10 líneas verticales equidistantes
for (int x = 50; x < width; x += 50) {
  line(x, 0, x, height);
}
```

---

## 4. Funciones de Eventos de Teclado y Ratón

* **`mousePressed()`**: Se ejecuta una sola vez cada vez que se pulsa un botón del ratón.
* **`keyPressed()`**: Se ejecuta una sola vez al pulsar una tecla del teclado (la tecla pulsada se almacena en la variable `key`).

```java
void keyPressed() {
  if (key == 'c' || key == 'C') {
    background(255); // Limpia la pantalla al pulsar la tecla C
  }
}
```

---

## ¿Por qué importa?
Transforma programas estáticos en aplicaciones y videojuegos interactivos controlados por el usuario.

---

## ¿Cómo se aplica o relaciona?
* Siguiente paso: animación y físicas en [[animacion_y_rebote_processing]].
* Comparar la sintaxis estructurada con [[programacion_arduino_funciones_basicas]].
