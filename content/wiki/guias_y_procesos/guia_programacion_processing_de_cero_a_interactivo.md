---
title: Guía de Programación en Processing: De Dibujos Básicos a Juegos Interactivos
tags: [guia, processing, programacion, tutorial, animacion, 4eso]
aliases: [Tutorial Processing, Prácticas Processing, Guía Processing 4º ESO]
---

# Guía de Programación en Processing: De Dibujos Básicos a Juegos Interactivos

Esta guía recopila todas las prácticas y ejercicios progresivos trabajados en 4º de ESO.

---

## Práctica 1: Creación de Formas y la Diana de Colores

### Objetivo:
Comprender el sistema de coordenadas, el orden de dibujado (*layers*) y el coloreado RGB.

```java
void setup() {
  size(400, 400);
  background(240);
  
  // Dibujar diana concéntrica (de fuera hacia dentro para no tapar figuras)
  strokeWeight(2);
  
  // 1. Círculo exterior Blanco
  fill(255);
  ellipse(200, 200, 300, 300);
  
  // 2. Círculo Negro
  fill(0);
  ellipse(200, 200, 220, 220);
  
  // 3. Círculo Azul
  fill(0, 150, 255);
  ellipse(200, 200, 150, 150);
  
  // 4. Círculo Rojo
  fill(255, 50, 50);
  ellipse(200, 200, 80, 80);
  
  // 5. Centro Amarillo
  fill(255, 230, 0);
  ellipse(200, 200, 30, 30);
}
```

---

## Práctica 2: Dibujo Dinámico e Interactividad con Ratón

```java
void setup() {
  size(500, 500);
  background(255);
}

void draw() {
  // Al mantener presionado el ratón, dibuja círculos cuyo tamaño depende de la velocidad
  if (mousePressed) {
    float radio = dist(pmouseX, pmouseY, mouseX, mouseY) + 5;
    fill(mouseX * 255 / width, mouseY * 255 / height, 180, 150);
    noStroke();
    ellipse(mouseX, mouseY, radio, radio);
  }
}

void keyPressed() {
  if (key == ' ') {
    background(255); // Barra espaciadora para borrar lienzo
  }
}
```

---

## Práctica 3: El Proyecto Final Multimedia (Minijuego de Rebote y Puntuación)

Cumple con todos los requisitos del trabajo de aula (bucles `for`, condicionales `if/else`, variables, animación e interacción):

```java
int pelotaX = 200, pelotaY = 50;
int velX = 4, velY = 4;
int palaX = 150, palaAncho = 100, palaAlto = 15;
int puntos = 0;
boolean gameOver = false;

void setup() {
  size(600, 400);
}

void draw() {
  if (!gameOver) {
    background(20, 30, 50);
    
    // 1. Fondo decorativo con bucle FOR (cuadrícula luminosa)
    stroke(40, 50, 80);
    for (int i = 0; i < width; i += 40) {
      line(i, 0, i, height);
    }
    
    // 2. Mover y dibujar la pala con el ratón
    palaX = constrain(mouseX - palaAncho / 2, 0, width - palaAncho);
    fill(0, 200, 255);
    rect(palaX, height - 30, palaAncho, palaAlto, 5);
    
    // 3. Mover la pelota
    pelotaX += velX;
    pelotaY += velY;
    
    // Rebotes en paredes laterales y superior
    if (pelotaX <= 10 || pelotaX >= width - 10) velX = -velX;
    if (pelotaY <= 10) velY = -velY;
    
    // Colisión con la pala
    if (pelotaY >= height - 30 - 10 && pelotaX >= palaX && pelotaX <= palaX + palaAncho) {
      velY = -abs(velY); // Rebota hacia arriba
      puntos++;
    }
    
    // Si la pelota cae por el fondo
    if (pelotaY > height) {
      gameOver = true;
    }
    
    // Dibujar pelota
    fill(255, 200, 0);
    ellipse(pelotaX, pelotaY, 20, 20);
    
    // Mostrar marcador
    fill(255);
    textSize(20);
    text("Puntuación: " + puntos, 20, 35);
    
  } else {
    // Pantalla de Game Over
    background(0);
    fill(255, 50, 50);
    textSize(36);
    textAlign(CENTER);
    text("¡FIN DE LA PARTIDA!", width / 2, height / 2 - 20);
    textSize(20);
    fill(255);
    text("Puntos obtenidos: " + puntos, width / 2, height / 2 + 20);
    text("Presiona 'R' para reiniciar", width / 2, height / 2 + 60);
  }
}

void keyPressed() {
  if (gameOver && (key == 'r' || key == 'R')) {
    pelotaX = 200;
    pelotaY = 50;
    velX = 4;
    velY = 4;
    puntos = 0;
    gameOver = false;
  }
}
```

---
*Conceptos relacionados: [[entorno_processing_estructura_y_graficos]], [[interactividad_y_variables_processing]], [[animacion_y_rebote_processing]].*
