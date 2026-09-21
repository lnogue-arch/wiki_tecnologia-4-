---
title: Guía de Programación Arduino: Control de Semáforos
tags: [guia, arduino, semaforo, programacion, 3a_evaluacion, 4eso]
aliases: [Práctica Semáforo, Cruce Semafórico, Semáforo con Pulsador]
---

# Guía de Programación Arduino: Control de Semáforos

Esta guía incluye las tres actividades progresivas desarrolladas en el taller de robótica de 4º ESO.

---

## Actividad 1: Semáforo Simple (3 LEDs)

### Asignación de Pines:
* **Pin 12**: LED Rojo (a través de resistencia de $220\,\Omega$ a GND).
* **Pin 11**: LED Ámbar / Amarillo ($220\,\Omega$ a GND).
* **Pin 10**: LED Verde ($220\,\Omega$ a GND).

### Código C++ Arduino:
```cpp
const int pinRojo = 12;
const int pinAmbar = 11;
const int pinVerde = 10;

void setup() {
  pinMode(pinRojo, OUTPUT);
  pinMode(pinAmbar, OUTPUT);
  pinMode(pinVerde, OUTPUT);
}

void loop() {
  // 1. Verde encendido durante 5 segundos
  digitalWrite(pinVerde, HIGH);
  digitalWrite(pinAmbar, LOW);
  digitalWrite(pinRojo, LOW);
  delay(5000);

  // 2. Ámbar parpadeante / fijo de transición durante 2 segundos
  digitalWrite(pinVerde, LOW);
  digitalWrite(pinAmbar, HIGH);
  delay(2000);

  // 3. Rojo encendido durante 5 segundos
  digitalWrite(pinAmbar, LOW);
  digitalWrite(pinRojo, HIGH);
  delay(5000);
}
```

---

## Actividad 2: Cruce con Dos Semáforos Sincronizados

Para regular un cruce entre dos calles perpendiculares (Semáforo 1: Pines 13, 12, 11; Semáforo 2: Pines 10, 9, 8).

```cpp
// Semáforo 1 (Calle Principal)
const int S1_Rojo = 13, S1_Ambar = 12, S1_Verde = 11;
// Semáforo 2 (Calle Secundaria)
const int S2_Rojo = 10, S2_Ambar = 9, S2_Verde = 8;

void setup() {
  pinMode(S1_Rojo, OUTPUT); pinMode(S1_Ambar, OUTPUT); pinMode(S1_Verde, OUTPUT);
  pinMode(S2_Rojo, OUTPUT); pinMode(S2_Ambar, OUTPUT); pinMode(S2_Verde, OUTPUT);
}

void loop() {
  // Estado 1: Calle 1 en Verde, Calle 2 en Rojo
  digitalWrite(S1_Verde, HIGH); digitalWrite(S1_Ambar, LOW); digitalWrite(S1_Rojo, LOW);
  digitalWrite(S2_Verde, LOW);  digitalWrite(S2_Ambar, LOW); digitalWrite(S2_Rojo, HIGH);
  delay(6000);

  // Estado 2: Calle 1 pasa a Ámbar, Calle 2 sigue en Rojo
  digitalWrite(S1_Verde, LOW);  digitalWrite(S1_Ambar, HIGH);
  delay(2000);

  // Estado 3: Ambos en Rojo durante 1 segundo (Seguridad de desalojo de cruce)
  digitalWrite(S1_Ambar, LOW);  digitalWrite(S1_Rojo, HIGH);
  delay(1000);

  // Estado 4: Calle 1 en Rojo, Calle 2 pasa a Verde
  digitalWrite(S2_Rojo, LOW);   digitalWrite(S2_Verde, HIGH);
  delay(6000);

  // Estado 5: Calle 2 pasa a Ámbar
  digitalWrite(S2_Verde, LOW);  digitalWrite(S2_Ambar, HIGH);
  delay(2000);

  // Estado 6: Ambos en Rojo antes de reiniciar
  digitalWrite(S2_Ambar, LOW);  digitalWrite(S2_Rojo, HIGH);
  delay(1000);
}
```

---

## Actividad 3: Semáforo con Pulsador de Peatones

Incorpora un pulsador con resistencia *pull-down* de $10\text{ k}\Omega$ en el Pin 2.

```cpp
const int pinRojoCoches = 12;
const int pinVerdeCoches = 10;
const int pinRojoPeaton = 7;
const int pinVerdePeaton = 6;
const int pinPulsador = 2;

void setup() {
  pinMode(pinRojoCoches, OUTPUT);
  pinMode(pinVerdeCoches, OUTPUT);
  pinMode(pinRojoPeaton, OUTPUT);
  pinMode(pinVerdePeaton, OUTPUT);
  pinMode(pinPulsador, INPUT);
}

void loop() {
  // Estado Normal: Coches en verde, peatones en rojo
  digitalWrite(pinVerdeCoches, HIGH);
  digitalWrite(pinRojoCoches, LOW);
  digitalWrite(pinVerdePeaton, LOW);
  digitalWrite(pinRojoPeaton, HIGH);

  // Si un peatón presiona el botón:
  if (digitalRead(pinPulsador) == HIGH) {
    delay(2000); // Tiempo de cortesía para los vehículos

    // Detener coches
    digitalWrite(pinVerdeCoches, LOW);
    digitalWrite(pinRojoCoches, HIGH);
    delay(1000);

    // Habilitar paso de peatones
    digitalWrite(pinRojoPeaton, LOW);
    digitalWrite(pinVerdePeaton, HIGH);
    delay(5000); // Tiempo de cruce

    // Parpadeo verde de peatones anunciando fin de tiempo
    for(int i = 0; i < 4; i++) {
      digitalWrite(pinVerdePeaton, LOW);
      delay(300);
      digitalWrite(pinVerdePeaton, HIGH);
      delay(300);
    }
  }
}
```

---
*Conceptos relacionados: [[arquitectura_arduino_y_pines]], [[programacion_arduino_funciones_basicas]], [[diodos_y_leds]].*
